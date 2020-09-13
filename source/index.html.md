---
title: App Core API Reference

language_tabs:
  - csharp

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>
  #- <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - audioContainerExtensions

search: true

code_clipboard: true
---

# Введение

Документация к [AppCore](https://gitlab.com/msa-developers/appcore). Здесь собрано описание основного функционала инструментария.

<!-- Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/slatedocs/slate). Feel free to edit it and use it as a base for your own API's documentation. -->

# Audio

## AudioController

<aside class="warning"> Obsolete class. Use `AudioStream` instead.</aside>

## IAudioGroup

Контейнер для потоков звуков. Выполняет роль медиатора для управления паузой/громкостью/мутом, а так же - позволяет найти конкретные вложенные потоки.

### ID

`string ID { get; }`
Уникальное название для группы. По умолчанию `null`.

```csharp
var group = AudioGroupManager.Instance.GetGroup("some_group");
Debug.Log(group.ID); //Выведет название группы.
```

### GetStream

### GetStreamByClip

### GetStreams

### GetStreamsByClip

### SetID

## IAudioStream

### ID

### Loop

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
