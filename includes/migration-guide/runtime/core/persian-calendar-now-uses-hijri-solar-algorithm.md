### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a><span data-ttu-id="c5231-101">波斯日历现在使用回历太阳算法</span><span class="sxs-lookup"><span data-stu-id="c5231-101">Persian calendar now uses the Hijri solar algorithm</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c5231-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="c5231-102">Details</span></span>|<span data-ttu-id="c5231-103">自 .NET Framework 4.6 起，<xref:System.Globalization.PersianCalendar?displayProperty=name> 类使用回历太阳算法。</span><span class="sxs-lookup"><span data-stu-id="c5231-103">Starting with the .NET Framework 4.6, the <xref:System.Globalization.PersianCalendar?displayProperty=name> class uses the Hijri solar algorithm.</span></span> <span data-ttu-id="c5231-104">自 .NET Framework 4.6 起，对于早于 1800 年或晚于 2023 年（公历）的日期，在 <xref:System.Globalization.PersianCalendar?displayProperty=name> 和其他日历之间转换日期所得结果可能略微不同。此外，<xref:System.Globalization.PersianCalendar.MinSupportedDateTime> 现在为 <code>March 22, 0622 instead of March 21, 0622</code>。</span><span class="sxs-lookup"><span data-stu-id="c5231-104">Converting dates between the <xref:System.Globalization.PersianCalendar?displayProperty=name> and other calendars may produce a slightly different result beginning with the .NET Framework 4.6 for dates earlier than 1800 or later than 2023 (Gregorian).Also, <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> is now <code>March 22, 0622 instead of March 21, 0622</code>.</span></span>|
|<span data-ttu-id="c5231-105">建议</span><span class="sxs-lookup"><span data-stu-id="c5231-105">Suggestion</span></span>|<span data-ttu-id="c5231-106">请注意，在 .NET 4.6 中使用 PersianCalendar 时，某些较早或较晚的日期可能略微不同。</span><span class="sxs-lookup"><span data-stu-id="c5231-106">Be aware that some early or late dates may be slightly different when using the PersianCalendar in .NET 4.6.</span></span> <span data-ttu-id="c5231-107">另外，当在不同 .NET Framework 版本上运行的进程之间序列化日期时，请勿将它们存储为 PersianCalendar 日期字符串（因为这些值可能不相同）。</span><span class="sxs-lookup"><span data-stu-id="c5231-107">Also, when serializing dates between processes which may run on different .NET Framework versions, do not store them as PersianCalendar date strings (since those values may be different).</span></span>|
|<span data-ttu-id="c5231-108">范围</span><span class="sxs-lookup"><span data-stu-id="c5231-108">Scope</span></span>|<span data-ttu-id="c5231-109">次要</span><span class="sxs-lookup"><span data-stu-id="c5231-109">Minor</span></span>|
|<span data-ttu-id="c5231-110">版本</span><span class="sxs-lookup"><span data-stu-id="c5231-110">Version</span></span>|<span data-ttu-id="c5231-111">4.6</span><span class="sxs-lookup"><span data-stu-id="c5231-111">4.6</span></span>|
|<span data-ttu-id="c5231-112">类型</span><span class="sxs-lookup"><span data-stu-id="c5231-112">Type</span></span>|<span data-ttu-id="c5231-113">运行时</span><span class="sxs-lookup"><span data-stu-id="c5231-113">Runtime</span></span>|
|<span data-ttu-id="c5231-114">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="c5231-114">Affected APIs</span></span>|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|
