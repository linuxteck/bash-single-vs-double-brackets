# 🔍 Bash Single vs Double Brackets — [[ ]] vs [ ] Explained (2026)

![Linux](https://img.shields.io/badge/Linux-Guide-blue)
![Level](https://img.shields.io/badge/Level-Intermediate%20to%20Advanced-green)
![Updated](https://img.shields.io/badge/Updated-2026-orange)
![Focus](https://img.shields.io/badge/Focus-Bash%20Scripting-important)

> Confused about when to use `[ ]` versus `[[ ]]` in Bash scripts?  
> Understanding the difference can prevent bugs, improve readability, and make your scripts more reliable.

📖 **[Full Guide (syntax + comparisons + real examples → linuxteck.com)](https://www.linuxteck.com/bash-single-vs-double-brackets/?utm_source=github&utm_medium=repo&utm_campaign=bash-brackets)**

---

## ⚡ 1-Minute Understanding

If you remember just this:

- `[ ]` → Traditional POSIX test command
- `[[ ]]` → Modern Bash conditional expression
- `[[ ]]` → Safer and more powerful for Bash scripting

💡 For Bash scripts, `[[ ]]` is usually the better choice.

---

## 🖼️ Preview

> Understanding Bash conditional testing with single and double brackets

![Preview](https://github.com/linuxteck/bash-single-vs-double-brackets/blob/main/16.png)

---

## 🧠 Why This Guide Exists

Many Bash beginners see both `[ ]` and `[[ ]]` and assume they're identical.

They're not.

This guide helps you:
- Understand the differences clearly
- Avoid common scripting mistakes
- Write cleaner Bash conditionals

---

## 🔄 Quick Comparison

| Feature | `[ ]` | `[[ ]]` |
|----------|--------|---------|
| POSIX Compatible | ✅ Yes | ❌ No |
| Bash Specific | ❌ No | ✅ Yes |
| Regex Support | ❌ No | ✅ Yes |
| Pattern Matching | Limited | ✅ Built-in |
| Safer String Handling | ❌ No | ✅ Yes |

---

## 👉 Want full explanations, edge cases, and best practices?  
Read here:  
https://www.linuxteck.com/bash-single-vs-double-brackets/?utm_source=github&utm_medium=repo

---

## 🚀 Basic Examples (Copy-Paste Ready)

### Using Single Brackets

```bash
name="LinuxTeck"

if [ "$name" = "LinuxTeck" ]; then
    echo "Match Found"
fi
```

### Using Double Brackets

```bash
name="LinuxTeck"

if [[ $name == LinuxTeck ]]; then
    echo "Match Found"
fi
```

---

## 🧪 Regex Matching Example

```bash
email="admin@example.com"

if [[ $email =~ @example\.com$ ]]; then
    echo "Valid Company Email"
fi
```

💡 This works with `[[ ]]` but not with traditional `[ ]`.

---

## ⚠️ Common Mistakes

| Mistake | Problem |
|----------|---------|
| Missing quotes in `[ ]` | Word splitting errors |
| Using regex with `[ ]` | Doesn't work |
| Mixing syntax styles | Confusing scripts |
| Using Bash features in POSIX shell | Compatibility issues |

---

## 🎯 When Should You Use Each?

```bash
# Use [ ] when:
# Writing POSIX-compatible scripts

# Use [[ ]] when:
# Writing Bash-specific scripts
# Using regex
# Pattern matching
# Safer string comparisons
```

---

## 🔄 Real-World Use Cases

```bash
# User input validation
# File checks
# Regex matching
# Automation scripts
# Deployment pipelines
```

---

## 🎯 Who Gets the Most Value

| You Are | Benefit |
|---------|--------|
| 🟢 Beginner | Understand Bash syntax correctly |
| 🔵 Sysadmin | Write safer scripts |
| 🔴 DevOps Engineer | Build reliable automation |
| 🟡 Developer | Improve Bash code quality |

---

## 🔗 More LinuxTeck Guides You'll Want

> 📂 *Part of the **LinuxTeck Master Series** — practical Linux guides*

- ⚡ https://www.linuxteck.com/modern-linux-tools/
- 📝 https://www.linuxteck.com/bash-quoting-rules-for-cleaner-shell-scripts/
- 🔀 https://www.linuxteck.com/bash-conditional-statements/
- 🧠 https://www.linuxteck.com/bash-if-statement-complete-guide-with-examples/
- 🔍 https://github.com/linuxteck?tab=repositories

---

## ✍️ About LinuxTeck

**https://www.linuxteck.com** publishes practical, real-world Linux guides — no fluff, no filler.  
If you're learning Bash scripting, these guides will help you avoid common mistakes and write better automation.

⭐ Found this useful? Star this repo — it helps more Linux users discover it  
🔁 Share with your team — especially if they write Bash scripts daily 😄  
👤 https://github.com/linuxteck

---

**Topics:** bash • shell-scripting • bash-conditionals • linux • scripting • automation • devops • sysadmin • terminal • bash-tips
