# dotnet core cli

dotnet 命令   
   
|  命令	 |  常规  |  
|  ----  | ----  |
|dotnet build	|生成 .NET Core 应用程序。|   
|dotnet build-server	|与通过生成启动的服务器进行交互。   
|dotnet clean	|清除生成输出。|   
|dotnet help	|显示命令更详细的在线文档。|   
|dotnet migrate	|将有效的预览版 2 项目迁移到 .NET Core SDK 1.0 项目。|   
|dotnet msbuild	|提供对 MSBuild 命令行的访问权限。|   
|dotnet new	|为给定的模板初始化 C# 或 F# 项目。|   
|dotnet pack	|创建代码的 NuGet 包。|   
|dotnet publish	|发布 .NET 依赖于框架或独立应用程序。|   
|dotnet restore	|还原给定应用程序的依赖项。|   
|dotnet run	|从源运行应用程序。|   
|dotnet sln	|用于添加、删除和列出解决方案文件中项目的选项。|   
|dotnet store	|将程序集存储到运行时包存储区。|   
|dotnet test	|使用测试运行程序运行测试。|   
   
|命令	|项目引用   |
|  ----  | ----  |
|dotnet add reference	|添加项目引用。|   
|dotnet list reference	|列出项目引用。|   
|dotnet remove reference	|删除项目引用。|   
   
|命令	|NuGet 包   |
|  ----  | ----  |
|dotnet add package	|添加 NuGet 包。|   
|dotnet remove package	|删除 NuGet 包。|   
   
|命令	|NuGet 命令   |
|  ----  | ----  |   
|dotnet nuget delete	|从服务器删除或取消列出包。|   
|dotnet nuget push	|将包推送到服务器，并将其发布。|   
|dotnet nuget locals	|清除或列出本地 NuGet 资源，例如 http 请求缓存、临时缓存或计算机范围的全局包文件夹。|   
|dotnet nuget add source	|添加 NuGet 源。|   
|dotnet nuget disable source	|禁用 NuGet 源。|   
|dotnet nuget enable source	|启用 NuGet 源。|   
|dotnet nuget list source	|列出所有已配置的 NuGet 源。|    
|dotnet nuget remove source	|删除 NuGet 源。|   
|dotnet nuget update source	|更新 NuGet 源。|   
   
# dotnet core api

|  Namespace  | 命名空间  |  
|  ----  | ----  |  
|System |	包含用于定义常用值和引用数据类型、事件和事件处理程序、接口、特性以及处理异常的基础类和基类。|
|System.Buffers |	包含用于创建和管理内存缓冲区的类型，例如由 和 表示的类型。|
|System.CodeDom |	包含可以用于表示源代码文档的元素和结构的类。 此中的类可用来建立源代码文档结构的模型，使用 提供的功能可以将源代码文档输出为所支持语言的源代码。|
|System.Collections |	包含接口和类，这些接口和类定义各种对象（如列表、队列、位数组、哈希表和字典）的集合。|
|System.ComponentModel |	提供用于实现组件和控件的运行时和设计时行为的类。 此包括用于特性和类型转换器的实现、数据源绑定和组件授权的基类和接口。|
|System.Configuration |	包含提供用于处理配置数据的编程模型的类型。|
|System.Data.Odbc |	为 ODBC .NET Framework 数据提供程序。|
|System.Data.OleDb |	为 OLE DB .NET Framework数据提供程序。|
|System.Data.OracleClient |	是用于 Oracle 的 .NET Framework 数据提供程序。|
|System.Data.SqlClient |	是用于 SQL Server 的 .NET 数据提供程序。|
|System.Diagnostics |	提供类，使您能够与系统进程、事件日志和性能计数器进行交互。|
|System.DirectoryServices |	利用 ，可以方便地从托管代码中访问 Active Directory 域服务。 该包含两个组件类，即 和 ，它们使用 Active Directory 服务接口 (ADSI) 技术。 ADSI 是 Microsoft 提供的一组接口，作为使用各种网络提供程序的灵活的工具。 无论网络有多大，ADSI 都可以使管理员能够相对容易地定位和管理网络上的资源。|
|System.Drawing |	提供了对 GDI+ 基本图形功能的访问权限。 、 和 中提供了更高级功能。|
|System.Dynamic |	提供支持动态语言运行时的类和接口。|
|System.Globalization |	包含定义区域性相关信息的类，这些信息包括语言，国家/地区，正在使用的日历，日期、货币和数字的格式模式，以及字符串的排序顺序。 这些类对于编写全球化（国际化）应用程序很有用。 而像 和 这样的类更是为我们提供了诸如代理项支持和文本元素处理等高级全球化功能。|
|System.IO |	|System.IO 包含允许读写文件和数据流的类型以及提供基本文件和目录支持的类型。|
|System.Linq |	提供支持使用语言集成查询 (LINQ) 进行查询的类和接口。|
|System.Media |	包含用于播放声音文件和访问系统提供的声音的类。|
|System.Net |	为当前网络上使用的多种协议提供了简单的编程接口。 和 类形成了所谓的可插接式协议的基础，可插接式协议是网络服务的一种实现，它使您能够开发出使用 Internet 资源的应用程序，而不必考虑各种不同协议的具体细节。 中的类可用于开发 Windows 应用商店应用程序或桌面应用程序。 当使用 Windows 应用商店应用程序时， 中的类将受网络隔离功能（Windows 开发人员预览版使用的一部分应用程序安全模型）的影响。 必须在应用程序清单中为本系统的 Windows 应用商店应用程序启动相应的网络功能，以便允许 Windows 应用商店应用程序的网络访问。 有关详细信息，请参阅适用于 Windows Store 应用的网络隔离。|
|System.Net.Http |	提供用于现代 HTTP 应用程序的编程接口。|
|System.Net.Mail |	包含用于将电子邮件发送到简单邮件传输协议 (SMTP) 服务器进行传送的类。|
|System.Net.Sockets |	为需要严密控制网络访问的开发人员提供了 Windows Sockets (Winsock) 接口的托管实现。|
|System.Net.WebSockets |	为开发人员提供了对 WebSocket 接口的托管实现。|
|System.Numerics |	包含补充由 .NET 定义的数值基元（例如 、 和 ）的数值类型。|
|System.Printing |	提供可用于自动管理打印服务器、打印队列和打印作业的类。|
|System.Reflection |	包含通过检查托管代码中程序集、模块、成员、参数和其他实体的元数据来检索其相关信息的类型。 这些类型还可用于操作加载类型的实例，例如挂钩事件或调用方法。 若要动态创建类型，请使用 。|
|System.Resources |	提供各种类和接口，这些类和接口使开发人员可以创建、存储和管理在应用程序中使用的不同特定于区域性的资源。 最重要的类之一是 类。|
|System.Runtime |	包含支持不同（如 |System、Runtime 和 Security ）的高级类型。|
|System.Runtime.Serialization |	包含可用于将对象序列化和反序列化的类。 序列化是将对象或对象图转换为线性的字节序列以存储或传输到其他位置的过程。 反序列化是接受存储的信息并从该信息重新创建对象的过程。|
|System.Security |	提供公共语言运行时安全系统的基础结构，包括权限的基类。|
|System.ServiceProcess |	提供用于实现、安装和控制 Windows 服务应用程序的类。 服务是长期运行的可执行文件，它们不通过用户界面来运行。 实现服务涉及以下方面：从 类继承，定义在传入开始、停止、暂停和继续命令时要处理的特定行为，以及定义在系统关闭时要执行的自定义行为和操作。|
|System.Text |	包含表示 ASCII 和 Unicode 字符编码的类；用于让字符块和字节块相互转换的抽象基类；以及无需创建 的中间实例即可操作并格式化 对象的帮助器类。|
|System.Text.Json |	|System.Text.Json 提供高性能、低分配以及符合标准的功能来处理 JavaScript 对象表示法 (JSON)，其中包括将对象序列化为 JSON 文本以及将 JSON 文本反序列化为对象（内置 UTF-8 支持）。 它还提供类型以用于读取和写入编码为 UTF-8 的 JSON 文本，以及用于创建内存中文档对象模型 (DOM) 以在数据的结构化视图中随机访问 JSON 元素。|
|System.Threading |	提供一些使得可以进行多线程编程的类和接口。 除同步线程活动和数据访问的类（、、 、等）之外,此还包含一个 类（它可让用户使用系统提供的线程池）和一个 类（在线程池线程上执行回调方法）。|
|System.Threading.Tasks |	该 |System.Threading.Tasks 提供简化编写并发和异步代码的工作的类型。 主要类型为 （表示可以等待和取消的异步操作）和 （可以返回值的任务）。 类提供用于创建和启动任务的静态方法， 类提供默认线程调度基础结构。|
|System.Timers |	提供 组件，它使您可以在指定的间隔是引发事件。|
|System.Transactions |	使用 包含的类可以编写自己的事务应用程序和资源管理器。 具体地说，可以创建和参与（与一个或多个参与者）本地或分布式事务。|
|System.Web |	提供使得可以进行浏览器与服务器通信的类和接口。 此包括 类（用于提供有关当前 HTTP 请求的广泛信息）、 类（用于管理输出到客户端的 HTTP 输出）以及 类（用于提供对服务器端实用工具与进程的访问）。 还包括用于 Cookie 操作、文件传输、异常信息和输出缓存控制的类。|
|System.Windows |	此提供了一些重要的 Windows Presentation Foundation (WPF) 基元素类、各种支持 WPF 属性系统和事件逻辑的类以及由 WPF 核心和框架更加广泛使用的其他类型。|
|System.Windows.Controls |	提供一些类以创建称为控件的元素，从而使用户可使用这些元素与应用程序进行交互。 控件类在用户的所有应用程序体验中处于核心地位，因为用户可使用它们来查看、选择或输入数据或其他信息。|
|System.Windows.Data |	包含用于将属性绑定到数据源、数据源提供程序类以及集合和视图的特定于数据的实现的类。|
|System.Windows.Documents |	包含支持 、 和 XML 纸张规范 (XPS) 文档创建的类。|
|System.Windows.Documents.Serialization |	提供类型用于支持创建并使用运行时可访问的插件序列化程序（该程序用于读取和写入各种数据格式文档）。|
|System.Windows.Forms |	包含用于创建基于 Windows 的应用程序的类，以充分利用 Microsoft Windows 操作系统中提供的丰富的用户界面功能。|
|System.Windows.Interop |	为 Windows Presentation Foundation (WPF) 和其他技术（如 Windows API）之间的互操作提供支持类型，并为涉及 WPF 的其他特定互操作方案提供基类。|
|System.Xml |	为处理 XML 提供基于标准的支持。|
|System.Xml.Linq |	包含 LINQ to XML 的类。 LINQ to XML 是内存中的 XML 编程接口，使您可以轻松有效地修改 XML 文档。|
|System.Xml.Serialization |	包含用于将对象序列化为 XML 格式文档或流的类。|
