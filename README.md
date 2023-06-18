# 这是什么？

该项目是一个基于JavaScript的网页工具，提供了一个简单而实用的界面，让用户能够输入密钥（Key），并直接在网页中生成与当前时间相关的TOTP密码，以用于身份验证、双因素认证等场景。

> ## TOTP是什么？
>
> TOTP（Time-Based One-Time Password）是一种基于时间的单次密码算法，用于增强身份验证的安全性。它是一种常见的双因素认证（2FA）方法之一。
>
> 常见的TOTP应用包括**Google Authenticator**、**Authy**和**微软身份验证器**等身份验证应用程序。这些应用程序提供了用户友好的界面和自动化的TOTP密码生成，为用户提供了更高的安全性和身份验证保护。
>
> 通常，用户将TOTP密钥与其账户关联，例如与邮箱、社交媒体、云服务等账户相关联。当用户登录时，系统会要求用户输入当前时间的TOTP密码，以验证其身份。服务端和用户设备之间需要保持时间同步，以确保生成的TOTP密码一致。
>
> TOTP的基本原理是根据当前时间和事先共享的密钥生成一个短期有效的密码。这个密码只能在一个特定的时间窗口内使用，过了这个时间窗口就会失效。由于密码的短期有效性和一次性使用，TOTP提供了额外的安全层，可以抵御许多常见的身份验证攻击，如密码重放攻击。
>
> 生成TOTP密码的过程如下：
> 1. 用户在设备或应用程序中输入密钥（Key）。
> 2. 使用哈希算法（通常是HMAC-SHA1、HMAC-SHA256等）和密钥对当前时间戳进行计算。
> 3. 根据算法规定的时间步长（通常为30秒），计算出当前时间所在时间步的密码。
> 4. 将密码进行格式化，通常为6位数字，并提供给用户使用。
> 5. 密码在下一个时间步长后将失效，需要生成新的密码。
>
