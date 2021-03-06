---
title: Config - detekt-api
---

[detekt-api](../../index.html) / [io.gitlab.arturbosch.detekt.api](../index.html) / [Config](./index.html)

# Config

`interface Config`

A configuration holds information about how to configure specific rules.

### Exceptions

| [InvalidConfigurationError](-invalid-configuration-error/index.html) | `class InvalidConfigurationError : `[`RuntimeException`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-runtime-exception/index.html)<br>Is thrown when loading a configuration results in errors. |

### Functions

| [subConfig](sub-config.html) | `abstract fun subConfig(key: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`Config`](./index.html)<br>Tries to retrieve part of the configuration based on given key. |
| [valueOrDefault](value-or-default.html) | `abstract fun <T : `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`> valueOrDefault(key: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, default: `[`T`](value-or-default.html#T)`): `[`T`](value-or-default.html#T)<br>Retrieves a sub configuration or value based on given key. If configuration property cannot be found the specified default value is returned. |
| [valueOrNull](value-or-null.html) | `abstract fun <T : `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`> valueOrNull(key: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`T`](value-or-null.html#T)`?`<br>Retrieves a sub configuration or value based on given key. If the configuration property cannot be found, null is returned. |

### Companion Object Properties

| [ACTIVE_KEY](-a-c-t-i-v-e_-k-e-y.html) | `const val ACTIVE_KEY: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [empty](empty.html) | `val empty: `[`Config`](./index.html)<br>An empty configuration with no properties. This config should only be used in test cases. Always returns the default value except when 'active' is queried, it returns true . |
| [EXCLUDES_KEY](-e-x-c-l-u-d-e-s_-k-e-y.html) | `const val EXCLUDES_KEY: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [INCLUDES_KEY](-i-n-c-l-u-d-e-s_-k-e-y.html) | `const val INCLUDES_KEY: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [PRIMITIVES](-p-r-i-m-i-t-i-v-e-s.html) | `val PRIMITIVES: `[`Set`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-set/index.html)`<`[`KClass`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)`<out `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`>>` |

### Inheritors

| [CompositeConfig](../-composite-config/index.html) | `class CompositeConfig : `[`Config`](./index.html)<br>Wraps two different configuration which should be considered when retrieving properties. |
| [ConfigAware](../-config-aware/index.html) | `interface ConfigAware : `[`Config`](./index.html)<br>Interface which is implemented by each Rule class to provide utility functions to retrieve specific or generic properties from the underlying detekt configuration file. |
| [HierarchicalConfig](../-hierarchical-config/index.html) | `interface HierarchicalConfig : `[`Config`](./index.html)<br>A configuration which keeps track of the config it got sub-config'ed from by the [subConfig](sub-config.html) function. It's main usage is to recreate the property-path which was taken when using the [subConfig](sub-config.html) function repeatedly. |

