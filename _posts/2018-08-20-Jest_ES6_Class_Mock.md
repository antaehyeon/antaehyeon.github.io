---
layout: post
title:  "[코드스쿼드] Jest 를 이용한 ES6 Class Mock"
subtitle:   "코드스쿼드"
categories: devlog
tags: HTMLCSS
comments: true
---

> Test Code 를 작성하면서 배운 것을 기록한 글입니다.

## ES6 Class Mocks

---

Jest 는 테스트 파일로 가져온 ES6 클래스를 모형화(mock) 하는데 사용할 수 있습니다.ES6 클래스는 약간의 가독성을 지닌 생성자 함수를 지니고 있습니다.

<br/>

## ES6 Class Example

---

ES6 클래스 예제(사운드파일을 재생하는)에는 `SoundPlayer` 와 해당 클래스를 사용하는 `SoundPlayerConsumer` 가 존재합니다. `SoundPlayerConsumer` 을 테스트하면서 `SoundPlayer` 을 모형화(mock) 할 것입니다.

```javascript
// sound-player.js
export default class SoundPlayer {
  constructor() {
    this.foo = 'bar';
  }

  playSoundFile(fileName) {
    console.log('Playing sound file ' + fileName);
  }
}
```

```javascript
// sound-player-consumer.js
import SoundPlayer from './sound-player';

export default class SoundPlayerConsumer {
  constructor() {
    this.soundPlayer = new SoundPlayer();
  }

  playSomethingCool() {
    const coolSoundFileName = 'song.mp3';
    this.soundPlayer.playSoundFile(coolSoundFileName);
  }
}
```

<br/>

## ES6 Class 모형(Mock)을 생성하는 4가지 방법

---

### 1. 자동 모형(Mock)

`jest.mock('sound-player')` 을 호출하면, 클래스 생성자에 대한 호출과 모든 방법을 모니터링 하는데 사용할 수 있는 유용한 `자동 모형, 모의 (automatic mock)` 가 반환됩니다.

ES6 클래스는 모의 생성자(Mock Constructor)로 대체되고, 모든 함수를 항상 undefined 를 반환하는 mock 함수로 변경합니다. 메소드 호출은 `AutomaticMock.mock.instances[index].methodName.mock.calls` 에 저장됩니다. 

클래스에서 화살표함수를 사용하면, 모의 객체에 포함되지 않습니다. 그 이유는 화살표 함수는 객체의 프로토타입에 존재하지 않기 때문에 (생성자가 존재하지 않기때문) 함수에 대한 참조를 보유하는 속성이기 때문입니다.

클래스의 구현을 교체할 필요가 없는 경우, 설정하기에 가장 쉬운 옵션입니다.

```javascript
import SoundPlayer from './sound-player';
import SoundPlayerConsumer from './sound-player-consumer';
jest.mock('./sound-player'); // SoundPlayer is now a mock constructor

beforeEach(() => {
  // Clear all instances and calls to constructor and all methods:
  SoundPlayer.mockClear();
});

it('We can check if the consumer called the class constructor', () => {
  const soundPlayerConsumer = new SoundPlayerConsumer();
  expect(SoundPlayer).toHaveBeenCalledTimes(1);
});

it('We can check if the consumer called a method on the class instance', () => {
  // Show that mockClear() is working:
  expect(SoundPlayer).not.toHaveBeenCalled();

  const soundPlayerConsumer = new SoundPlayerConsumer();
  // Constructor should have been called again:
  expect(SoundPlayer).toHaveBeenCalledTimes(1);

  const coolSoundFileName = 'song.mp3';
  soundPlayerConsumer.playSomethingCool();

  // mock.instances is available with automatic mocks:
  const mockSoundPlayerInstance = SoundPlayer.mock.instances[0];
  const mockPlaySoundFile = mockSoundPlayerInstance.playSoundFile;
  expect(mockPlaySoundFile.mock.calls[0][0]).toEqual(coolSoundFileName);
  // Equivalent to above check:
  expect(mockPlaySoundFile).toHaveBeenCalledWith(coolSoundFileName);
  expect(mockPlaySoundFile).toHaveBeenCalledTimes(1);
});
```

<br/>

### 2. 수동 모형 (Manual Mock)

`__mocks__` 폴더에 모의구현을 저장하여 수동 모형(Manual Mock)을 생성합니다. 이를 통해 구현을 지정할 수 있으며, 테스트 파일 전체에서 사용할 수 있습니다.

```javascript
// __mocks__/sound-player.js

// Import this named export into your test file:
export const mockPlaySoundFile = jest.fn();
const mock = jest.fn().mockImplementation(() => {
  return {playSoundFile: mockPlaySoundFile};
});

export default mock;
```

모든 인스턴스에서 공유하는 Mock 및 Mock 메소드를 가져옵니다.

```javascript
// sound-player-consumer.test.js
import SoundPlayer, {mockPlaySoundFile} from './sound-player';
import SoundPlayerConsumer from './sound-player-consumer';
jest.mock('./sound-player'); // SoundPlayer is now a mock constructor

beforeEach(() => {
  // Clear all instances and calls to constructor and all methods:
  SoundPlayer.mockClear();
  mockPlaySoundFile.mockClear();
});

it('We can check if the consumer called the class constructor', () => {
  const soundPlayerConsumer = new SoundPlayerConsumer();
  expect(SoundPlayer).toHaveBeenCalledTimes(1);
});

it('We can check if the consumer called a method on the class instance', () => {
  const soundPlayerConsumer = new SoundPlayerConsumer();
  const coolSoundFileName = 'song.mp3';
  soundPlayerConsumer.playSomethingCool();
  expect(mockPlaySoundFile).toHaveBeenCalledWith(coolSoundFileName);
});
```

<br/>

### 3. Module Factory 매개변수를 통한 jest.mock() 호출하기

`jest.mock(path, moduleFactory)` 는 module factory argument 를 사용합니다. module factory 는 Mock 을 반환하는 기능을 가지고 있습니다. 

생성자 함수를 모형(Mock) 하기 위해서 module factory 는 항상 생성자 함수를 리턴해야 합니다. 즉, module factory 는 함수 (higher-order function) (HOF) 를 반환하는 함수여야 합니다.

```javascript
import SoundPlayer from './sound-player';
const mockPlaySoundFile = jest.fn();
jest.mock('./sound-player', () => {
  return jest.fn().mockImplementation(() => {
    return {playSoundFile: mockPlaySoundFile};
  });
});
```

 factory parameter 의 한계는 `jest.mock()` 호출을 파일 상단에 호이스트(hosited) 되기 때문에, 변수로 먼저 정의하고 factory 에서 사용할 수 없습니다. `mock` 이라는 단어로 시작하는 변수에는 예외가 존재합니다. 그것들이 제때에 초기화될 수 있도록 보장하는 것은 여러분에게 달려있습니다.





































