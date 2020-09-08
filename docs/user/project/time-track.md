# 时间跟踪[](#time-track "Permalink")

时间跟踪允许您跟踪估计和花费在问题上的时间以及在 CODEChina 中合并请求。

## 概览[](#overview "Permalink")

时间跟踪使您能够：

*   记录处理 Issue 或合并请求所花费的时间
*   添加完成 Issue 或合并请求所需时间的估计

您不必输入估算值即可输入花费的时间，反之亦然。

有关时间跟踪的数据显示在 Issue 及合并请求侧栏上。

## 如何更新数据[](#how-to-enter-data "Permalink")

时间跟踪可以如下两个[快速操作](/docs/user/project/quick-actions.md) ： `/spend`和`/estimate` 

快速操作既可以用于 Issue 或合并请求的正文中，也可以用于 Issue 或合并请求的注释中。

添加时间条目（花费的时间或估计的时间）仅限于项目成员。

### 预估[](#estimates "Permalink")

要输入估算值，请输入`/estimate` ，然后输入时间。例如，如果您需要输入 3 天 5 小时 10 分钟的估算值，则可以输入`/estimate 3d 5h 10m` ，我们支持的时间单位列在此帮助页面的底部。

每次输入新的时间估算值时，任何先前的时间估算值都将被该新值覆盖, 在发布或合并请求中应该只有一个有效的预估值。

要完全删除估算，请使用`/remove_estimate` 。

### 花费时间[](#time-spent "Permalink")

要输入花费的时间，请使用`/spend 3d 5h 10m` 。

每个新花费的时间条目将被添加到当前 Issue 或合并请求的总时间中。

您可以通过输入负数来减少时间： `/spend -3d`将从总花费时间中删除 3 天，您所花费的时间不能少于 0 分钟，因此，如果您删除的时间量与已输入的时间相比更长，则系统将自动重置所花费的时间。

要删除一次花费的所有时间，请使用`/remove_time_spent` 。

## 配置[](#configuration "Permalink")

以下时间单位可用：

*   月（mo）
*   周（w）
*   Days (d)
*   小时（h）
*   分钟（m）

默认转换率是 1mo = 4w，1w = 5d 和 1d = 8h。