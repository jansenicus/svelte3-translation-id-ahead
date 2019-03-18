---
title: Сабытия перехода
---

Иногда полезно знать, когда переходы начинаются и заканчиваются. Svelte генерирует события в процессе переходов, которые вы можете прослушивать, как любые другие события DOM:

```html
<p
	transition:fly="{{ y: 200, duration: 2000 }}"
	on:introstart="{() => status = 'начало появления'}"
	on:outrostart="{() => status = 'начало исчезновения'}"
	on:introend="{() => status = 'конец появления'}"
	on:outroend="{() => status = 'конец исчезновения'}"
>
	Прилетает и улетает
</p>
```