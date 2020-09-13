---
title: App Core API Reference

#language_tabs:
#  - csharp

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>
  #- <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

# includes:
#   - audioContainerExtensions

search: true

code_clipboard: true
---

# Введение

Документация к [AppCore](https://gitlab.com/msa-developers/appcore). Здесь собрано описание основного функционала инструментария.

# Audio

## AudioController

<aside class="warning"> Устарелый класс. В скором времени будет удалён. Используйте <code>AudioStream</code>'ы вместо него.</aside>

## IAudioGroup

Контейнер для потоков звуков. Выполняет роль медиатора для управления паузой/громкостью/мутом, а так же - позволяет найти конкретные вложенные потоки.

### ID
```csharp
string ID { get; }
```

Уникальное название для группы. По умолчанию `null`.

<aside class="notice"><code>ID</code> групп не должны и не могут повторяться.</aside>

### GetStream
```csharp
IAudioStream GetStream(string id);
```
> Пример использования
```csharp
var stream = group.GetStream("some_group");
```

Поиск ПЕРВОГО вложенного потока по определённому ID. Если такого нет - возвращает `null`.

### GetStreamByClip
```csharp
IAudioStream GetStreamByClip(AudioClip clip);
IAudioStream GetStreamByClip(string clipName);
```
> Пример использования
```csharp
var streamByClip = group.GetStreamByClip(audioClip);
var streamByClipName = group.GetStreamByClip(audioClip.name);
```

Поиск ПЕРВОГО вложенного потока по определённому аудио-клипу (или его названию). Если такого нет - возвращает `null`.

### GetStreams
```csharp
IAudioStream[] GetStreams(string id);
```
> Пример использования
```csharp
var streams = group.GetStreams("some_group");
```

Поиск всех вложенных потоков по определённому ID. В случае если их нет - возвращает пустой массив.

### GetStreamsByClip
```csharp
IAudioStream[] GetStreamsByClip(AudioClip clip);
IAudioStream[] GetStreamsByClip(string clipName);
```
> Пример использования
```csharp
var streamsByClip = group.GetStreamsByClip(audioClip);
var streamsByClipName = group.GetStreamsByClip(audioClip.name);
```

Поиск всех вложенных потоков по определённому аудио-клипу (или его названию). В случае если их нет - возвращает пустой массив.

## IAudioStream

Класс для управления аудио-потоком.

### ID
```csharp
string ID { get; }
```

Определённое имя потока. Не уникально и может повторяться.

### Loop
```csharp
bool Loop { get; }
```

Зацикленность звука.

### Clip

### Group

### OverrideGroupFlags

### SetID

### SetOnComplete

### SetOverrideGroupFlags

### Stop

## IAudioGroupManager

### DefaultGroup

### MusicGroup

### GetGroup

### GetStream

### GetStreamByClip

### GetStreamByClip

### GetStreams

### GetStreamsByClip

### GetStreamsByClip

## IAudioSettingsLayer

### Volume

### Mute

### Pause

## IAudioStream

### ID

### Loop

### Clip

### Group

### OverrideGroupFlags

### SetGroup

### SetID

### SetClip

### SetLoop

### SetVolume

### SetMute

### SetPause

### SetOnComplete

### SetOverrideGroupFlags

### Stop

## IAudioStreamManager

### GetStreamBuilder

## AudioStream.Builder

### Builder

### SetGroup

### SetID

### SetClip

### SetLoop

### SetVolume

### SetMute

### SetPause

### SetOnComplete

### SetOverrideGroupFlags

### Dispose

### Play

### Stop

## AudioStream

### GetBuilder

### Play

### CreateFromSource

## IAudioVolumeManager

### OverrideSettingsFlag

# Extensions

## ColorHelpers

## CyclicList

## DictionaryExtensions

## ListExtensions

## MathExtensions

## TransformExtensions

## TweenExtensions

## UnsortedExtensions

# Generated

# Helpers

# IAP

# Initialization

# Input

# Log

# Pooling

# Scene Managment

# Storage

# Taptic

# Time

# UI
