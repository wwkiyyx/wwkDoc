### **Microsoft.CSharp 命名空间包含支持使用 C# 语言编译和生成代码的类。**   
* CSharpCodeProvider	  
提供对 C# 代码生成器和代码编译器的实例的访问权限。   

### **Microsoft.Win32 命名空间提供两种类型的类：处理由操作系统引发的事件的类和操作系统注册表的类。**   
* OpenFileDialog	   
表示一个通用对话框，用户可以使用此对话框来指定一个或多个要打开的文件的文件名。   
* SaveFileDialog	   
表示一个通用对话框，用户可以使用此对话框来指定一个要将文件另存为的文件名。 在部分信任情况下执行的应用程序不能使用 SaveFileDialog。   
* Registry	   
提供表示 Windows 注册表中的根项的 RegistryKey 对象，并提供访问项/值对的 static 方法。   
* RegistryKey	   
表示 Windows 注册表中的项级节点。 此类是注册表封装。   
* SystemEvents	   
提供对系统事件通知的访问。 无法继承此类。   

### **System 命名空间包含用于定义常用值和引用数据类型、事件和事件处理程序、接口、特性以及处理异常的基础类和基类。**   
* Console	    
表示控制台应用程序的标准输入流、输出流和错误流。 无法继承此类。    
* Convert	    
将一个基本数据类型转换为另一个基本数据类型。    
* Delegate	    
表示一个委托，该委托是表示某一静态方法或某一类实例和该类的实例方法的数据结构。    
* Enum	    
提供枚举的基类。    
* Environment	    
提供有关当前环境和平台的信息以及操作它们的方法。 此类不能被继承。    
* Exception	    
表示在应用程序执行期间出现的错误。    
* GC	     
控制系统垃圾回收器（一种自动回收未使用内存的服务）。     
* Math	    
为三角函数、对数函数和其他通用数学函数提供常数和静态方法。    
* Object	    
支持 .NET 类层次结构中的所有类，并为派生类提供低级别服务。 这是所有 .NET 类的最终基类；它是类型层次结构的根。    
* OperatingSystem	    
表示有关操作系统的信息，如版本和平台标识符。 无法继承此类。    
* Random	    
表示伪随机数生成器，这是一种能够产生满足某些随机性统计要求的数字序列的算法。    
* String	    
将文本表示为 UTF-16 代码单元的序列。    
* Tuple	   
提供用于创造元组对象的静态方法。   
* Type	   
表示类型声明：类类型、接口类型、数组类型、值类型、枚举类型、类型参数、泛型类型定义，以及开放或封闭构造的泛型类型。   
* Version	    
表示程序集、操作系统或公共语言运行时的版本号。 无法继承此类。    
* Byte	   
表示一个 8 位无符号整数。   
* Char	    
将字符表示为 UTF-16 代码单位。    
* DateTime	    
表示时间上的一刻，通常以日期和当天的时间表示。    
* Decimal	   
表示十进制浮点数。   
* Double	   
表示一个双精度浮点数。    
* Int32	    
表示 32 位有符号整数。    
* IntPtr	    
用于表示指针或句柄的特定于平台的类型。    
* TimeSpan	    
表示一个时间间隔。   

### **System.Buffers.Text Namespace 此命名空间包含一些类型，它们可用于分析常见数据类型并设置其格式，使其采用/不采用 UTF-8 文本表示形式。**   
* Base64	   
在二进制数据和以 base 64 表示的 UTF-8 编码的文本之间转换。   

### **System.CodeDom 命名空间包含可以用于表示源代码文档的元素和结构的类。 此命名空间中的类可用来建立源代码文档结构的模型，使用 System.CodeDom.Compiler 命名空间提供的功能可以将源代码文档输出为所支持语言的源代码。**   

### **System.CodeDom.Compiler 命名空间包含了这样一些类型：它们的用途是对所支持编程语言的源代码的生成和编译进行管理。 每个代码生成器都可以基于代码文档对象模型 (CodeDOM) 源代码模型（由 System.CodeDom 命名空间提供的元素组成）的结构来生成使用某种特定的编程语言的源代码。**   
* CodeCompiler	   
提供 ICodeCompiler 接口的示例实现。   
* Executor	   
为调用编译器提供命令执行功能。 无法继承此类。   

### **System.Collections 命名空间包含接口和类，这些接口和类定义各种对象（如列表、队列、位数组、哈希表和字典）的集合。**   
* ArrayList	   
使用大小会根据需要动态增加的数组来实现 IList 接口。   
* BitArray	   
管理位值的压缩数组，这些值以布尔值的形式表示，其中 true 表示此位为开 (1)，false 表示此位为关 (0)。   
* Hashtable	   
表示根据键的哈希代码进行组织的键/值对的集合。   
* Queue	   
表示对象的先进先出集合。   
* SortedList	   
表示键/值对的集合，这些键值对按键排序并可按照键和索引访问。   
* Stack	   
表示对象的简单后进先出 (LIFO) 非泛型集合。   
* DictionaryEntry	   
定义可设置或检索的字典键/值对。   

### **System.Collections.Concurrent 命名空间提供多个线程安全集合类。当有多个线程并发访问集合时，应使用这些类代替 System.Collections 和 System.Collections.Generic 命名空间中的对应类型。 但是，不保证通过扩展方法或通过显式接口实现访问集合对象是线程安全的，可能需要由调用方进行同步。**   
* ConcurrentBag<T>	   
表示对象的线程安全的无序集合。   
* ConcurrentDictionary<TKey,TValue>	   
表示可由多个线程同时访问的键/值对的线程安全集合。   
* ConcurrentQueue<T>	   
表示线程安全的先进先出 (FIFO) 集合。   
* ConcurrentStack<T>	   
表示线程安全的后进先出 (LIFO) 集合。   

### **System.Collections.Generic 命名空间包含定义泛型集合的接口和类，用户可以使用泛型集合来创建强类型集合，这种集合能提供比非泛型强类型集合更好的类型安全性和性能。**   
* Dictionary<TKey,TValue>	   
表示键和值的集合。   
* HashSet<T>	    
表示值的集。    
* List<T>	   
表示可通过索引访问的对象的强类型列表。 提供用于对列表进行搜索、排序和操作的方法。   
* Queue<T>	    
表示对象的先进先出集合。    
* Stack<T>	    
表示可变大小的后进先出 (LIFO) 集合（对于相同指定类型的实例）。   

### **System.Configuration 命名空间包含提供用于处理配置数据的编程模型的类型。**   
* ApplicationSettingsGroup	   
表示配置文件内的一组相关应用程序设置节。 此类不能被继承。   
* AppSettingsReader	   
提供一种从配置文件中读取特定类型的值的方法。   
* AppSettingsSection	    
为 appSettings 配置节提供配置系统支持。 无法继承此类。   
* Configuration	   
表示适用于特定计算机、应用程序或资源的配置文件。 无法继承此类。    
* ConnectionStringSettings	   
表示连接字符串配置文件节中的单个命名连接字符串。   

### **System.Data 命名空间提供对表示 ADO.NET 结构的类的访问。 通过 ADO.NET，可以生成可有效管理多个数据源的数据的组件。**   
* DataSet	    
表示数据的内存中缓存。    
* DataTable	   
表示内存中数据的一个表。   
* DataView	     
代表 DataTable 的可绑定数据的自定义视图，它用于排序、筛选、搜索、编辑和导航。 DataView 不存储数据，而改为表示对应的 DataTable 的连接视图。 更改 DataView 的数据会影响 DataTable。 更改 DataTable 的数据将影响与之关联的所有 DataView。    

### **System.Data.Common 命名空间包含由 .NET Framework 数据提供程序共享的类。**   
* DataAdapter	   
表示用于填充 DataSet 和更新数据源的一组 SQL 命令和一个数据库连接。   
* DbCommand	   
表示要对数据源执行的 SQL 语句或存储过程。 提供表示命令的数据库特定类的基类。 ExecuteNonQueryAsync   
* DbConnection	   
定义数据库连接的核心行为，并为数据库专用连接提供基类。      
* DbDataReader	   
从数据源中读取行的只进流。   

### **System.Diagnostics 命名空间提供类，使您能够与系统进程、事件日志和性能计数器进行交互。**   
* EventLog	   
提供与 Windows 事件日志的交互。   
* PerformanceCounter	    
表示 Windows NT 性能计数器组件。    
* Process	   
提供对本地和远程进程的访问权限并使你能够启动和停止本地系统进程。    

### **System.Drawing 命名空间提供了对 GDI+ 基本图形功能的访问权限。 System.Drawing.Drawing2D、System.Drawing.Imaging 和 System.Drawing.Text 命名空间中提供了更高级功能。**    
* Bitmap	   
封装 GDI+ 位图，此位图由图形图像及其属性的像素数据组成。 Bitmap 是用于处理由像素数据定义的图像的对象。    
* Brush	   
定义用于填充图形形状（如矩形、椭圆、饼形、多边形和封闭路径）的内部的对象。   
* Font	   
定义特定的文本格式，包括字体、字号和样式特性。 无法继承此类。   
* Graphics	   
封装一个 GDI+ 绘图图面。 无法继承此类。   
* Icon	   
表示 Windows 图标，它是用于表示对象的小位图图像。 尽管图标的大小由系统决定，但仍可将其视为透明的位图。     
* Image	   
为源自 Bitmap 和 Metafile 的类提供功能的抽象基类。   
* Pen	   
定义用于绘制直线和曲线的对象。 无法继承此类。    
* Color	    
表示一种 ARGB 颜色（alpha、红色、绿色、蓝色）。    
* Point	    
提供有序的 x 坐标和 y 坐标整数对，该坐标对在二维平面中定义一个点。    
* Size	    
存储一个有序整数对，用于指定 Height 和 Width。    
* Rectangle	    
存储一组整数，共四个，表示一个矩形的位置和大小。    

### **System.IO 命名空间包含允许读写文件和数据流的类型以及提供基本文件和目录支持的类型。**   
* BinaryReader	   
以特定的编码将基元数据类型读作二进制值。   
* BinaryWriter	   
将二进制中的基元类型写入流并支持用特定的编码写入字符串。    
* BufferedStream	    
将缓冲层添加到另一个流上的读取和写入操作。 无法继承此类。    
* Directory	    
公开用于通过目录和子目录进行创建、移动和枚举的静态方法。 无法继承此类。    
* DirectoryInfo	   
公开用于通过目录和子目录进行创建、移动和枚举的实例方法。 无法继承此类。      
* DriveInfo	    
提供对有关驱动器的信息的访问。     
* File	     
提供用于创建、复制、删除、移动和打开单一文件的静态方法，并协助创建 FileStream 对象。     
* FileInfo	     
提供用于创建、复制、删除、移动和打开文件的属性和实例方法，并且帮助创建 FileStream 对象。 无法继承此类。    
* FileStream	    
为文件提供 Stream，既支持同步读写操作，也支持异步读写操作。    
* FileSystemWatcher	    
侦听文件系统更改通知，并在目录或目录中的文件发生更改时引发事件。       
* MemoryStream	    
创建一个其后备存储为内存的流。   
* Path	   
对包含文件或目录路径信息的 String 实例执行操作。 这些操作是以跨平台的方式执行的。   
* Stream	   
提供字节序列的一般视图。 这是一个抽象类。   
* StreamReader	   
实现一个 TextReader，使其以一种特定的编码从字节流中读取字符。   
* StreamWriter	    
实现一个 TextWriter，使其以一种特定的编码向流中写入字符。   
* StringReader	   
实现从字符串进行读取的 TextReader。
* StringWriter	   
实现用于将信息写入字符串的 TextWriter。 信息存储在基础 StringBuilder 中。
* TextReader	    
表示可读取有序字符系列的读取器。
* TextWriter	     
表示可以编写一个有序字符系列的编写器。 此类是抽象类。   

### **System.IO.Compression 命名空间包含提供基本的流压缩和解压缩服务的类。**    
* ZipFile	   
提供创建、解压缩和打开 zip 存档的静态方法。   

### **System.IO.Pipes 命名空间包含的类型可提供通过匿名和/或命名管道实现进程间通信的途径。**    
* NamedPipeClientStream	   
暴露命名管道周围的 Stream，该管道既支持同步读写操作，也支持异步读写操作。   
* NamedPipeServerStream	   
公开命名管道周围的 Stream，该管道既支持同步读写操作，也支持异步读写操作。     

### **System.Linq 命名空间提供支持使用语言集成查询 (LINQ) 进行查询的类和接口。**   

### **System.Media 命名空间包含用于播放声音文件和访问系统提供的声音的类。**   
* SoundPlayer	   
控制 .wav 文件中的声音播放。   

### **System.Net 命名空间为当前网络上使用的多种协议提供了简单的编程接口。 WebRequest 和 WebResponse 类形成了所谓的可插接式协议的基础，可插接式协议是网络服务的一种实现，它使您能够开发出使用 Internet 资源的应用程序，而不必考虑各种不同协议的具体细节。 System.Net 命名空间中的类可用于开发 Windows 应用商店应用程序或桌面应用程序。 当使用 Windows 应用商店应用程序时，System.Net 命名空间中的类将受网络隔离功能（Windows 开发人员预览版使用的一部分应用程序安全模型）的影响。 必须在应用程序清单中为本系统的 Windows 应用商店应用程序启动相应的网络功能，以便允许 Windows 应用商店应用程序的网络访问。 有关详细信息，请参阅适用于 Windows Store 应用的网络隔离。**   
* HttpWebRequest    	   
提供 WebRequest 类的 HTTP 特定的实现。    
* HttpWebResponse	    
提供 WebResponse 类的 HTTP 特定的实现。    
* IPAddress	     
提供 Internet 协议 (IP) 地址。    
* IPEndPoint	    
将网络终结点表示为 IP 地址和端口号。    

### **System.Net.Http 命名空间提供用于现代 HTTP 应用程序的编程接口。**   
* HttpClient	   
提供用于发送 HTTP 请求并从 URI 标识的资源接收 HTTP 响应的基类。   

### **System.Net.NetworkInformation 命名空间提供对网络流量数据、网络地址信息和本地计算机的地址更改通知的访问。 该命名空间还包含实现 Ping 实用工具的类。 可以使用 Ping 和相关的类检查是否可通过网络连接到计算机。**    
* Ping	    
允许应用程序确定是否可通过网络访问远程计算机。   

### **System.Net.Sockets 命名空间为需要严密控制网络访问的开发人员提供了 Windows Sockets (Winsock) 接口的托管实现。**   
* NetworkStream	   
为网络访问提供数据的基础流。   
* Socket	   
实现 Berkeley 套接字接口。   
* TcpClient	   
为 TCP 网络服务提供客户端连接。   
* TcpListener	   
侦听来自 TCP 网络客户端的连接。   
* UdpClient	   
提供用户数据报协议 (UDP) 网络服务。     

### **System.Reflection 命名空间包含通过检查托管代码中程序集、模块、成员、参数和其他实体的元数据来检索其相关信息的类型。 这些类型还可用于操作加载类型的实例，例如挂钩事件或调用方法。 若要动态创建类型，请使用 System.Reflection.Emit 命名空间。**    
* Assembly	   
表示一个程序集，它是一个可重用、无版本冲突并且可自我描述的公共语言运行时应用程序构建基块。   
* EventInfo	     
发现事件的属性并提供对事件元数据的访问权限。   
* FieldInfo	    
发现字段的属性并提供对字段元数据的访问权限。    
* MemberInfo	    
获取有关成员属性的信息并提供对成员元数据的访问权限。    
* MethodInfo	    
发现方法的属性并提供对方法元数据的访问。    
* Module	    
对模块执行反射。    
* ParameterInfo	    
发现参数的属性并提供对参数元数据的访问权限。    
* PropertyInfo	    
发现属性 (Property) 的属性 (Attribute) 并提供对属性 (Property) 元数据的访问。    
* TypeInfo	    
表示类类型、接口类型、数组类型、值类型、枚举类型、类型参数、泛型类型定义，以及开放或封闭构造的泛型类型的类型声明。   

### **System.Security.Cryptography 命名空间提供加密服务，包括安全的数据编码和解码，以及许多其他操作，例如散列法、随机数字生成和消息身份验证。 有关更多信息，请参阅加密服务。**   
* Aes	   
表示高级加密标准 (AES) 的所有实现必须从中继承的抽象基类。   
* CngAlgorithm	   
封装加密算法的名称。    
* DES	    
表示数据加密标准 (DES) 算法的基类，所有 DES 实现都必须从此基类派生。    
* DSA	   
表示数字签名算法（DSA）的所有实现都必须从中继承的抽象基类。    
* HMAC	    
表示基于哈希的消息验证代码 (HMAC) 的所有实现必须从中派生的抽象类。   
* MD5	   
表示 MD5 哈希算法的所有实现均从中继承的抽象类。    
* RSA	    
表示 RSA 算法的所有实现均从中继承的基类。   
* SHA1	    
计算输入数据的 SHA1 哈希值。    

### **System.ServiceProcess 命名空间提供用于实现、安装和控制 Windows 服务应用程序的类。 服务是长期运行的可执行文件，它们不通过用户界面来运行。 实现服务涉及以下方面：从 ServiceBase 类继承，定义在传入开始、停止、暂停和继续命令时要处理的特定行为，以及定义在系统关闭时要执行的自定义行为和操作。**    

### **System.Text 命名空间包含表示 ASCII 和 Unicode 字符编码的类；用于让字符块和字节块相互转换的抽象基类；以及无需创建 String 的中间实例即可操作并格式化 String 对象的帮助器类。**   
* ASCIIEncoding	   
表示 Unicode 字符的 ASCII 字符编码。   
* UTF8Encoding	   
表示 Unicode 字符的 UTF-8 编码。   
* UnicodeEncoding	    
表示 Unicode 字符的 UTF-16 编码。    

### **System.Text.Json 命名空间提供高性能、低分配以及符合标准的功能来处理 JavaScript 对象表示法 (JSON)，其中包括将对象序列化为 JSON 文本以及将 JSON 文本反序列化为对象（内置 UTF-8 支持）。 它还提供类型以用于读取和写入编码为 UTF-8 的 JSON 文本，以及用于创建内存中文档对象模型 (DOM) 以在数据的结构化视图中随机访问 JSON 元素。**   
* JsonDocument	    
提供用于检查 JSON 值的结构内容，而不自动实例化数据值的机制。    
* JsonSerializer	    
提供将对象或值类型序列化为 JSON 以及将 JSON 反序列化为对象或值类型的功能。    

### **System.Threading 命名空间提供一些使得可以进行多线程编程的类和接口。 除同步线程活动和数据访问的类（Mutex、Monitor、 Interlocked、AutoResetEvent等）之外,此命名空间还包含一个 ThreadPool 类（它可让用户使用系统提供的线程池）和一个 Timer 类（在线程池线程上执行回调方法）。**    
* Mutex	    
还可用于进程间同步的同步基元。   
* Semaphore	    
限制可同时访问某一资源或资源池的线程数。   
* ReaderWriterLock	    
定义支持单个写线程和多个读线程的锁。   
* Thread	    
创建和控制线程，设置其优先级并获取其状态。   
* ThreadPool	   
提供一个线程池，该线程池可用于执行任务、发送工作项、处理异步 I/O、代表其他线程等待以及处理计时器。   

### **该 System.Threading.Tasks 命名空间提供简化编写并发和异步代码的工作的类型。 主要类型为 Task（表示可以等待和取消的异步操作）和 Task<TResult>（可以返回值的任务）。 TaskFactory 类提供用于创建和启动任务的静态方法，TaskScheduler 类提供默认线程调度基础结构。**   
* Task	    
表示一个异步操作。    
* Task\<TResult\>	    
表示一个可以返回值的异步操作。    

### **System.Timers 命名空间提供 Timer 组件，它使您可以在指定的间隔是引发事件。**   
* Timer	    
在设定的间隔之后生成事件，带有生成重复事件的选项。    

### **System.Windows Namespace 此命名空间提供了一些重要的 Windows Presentation Foundation (WPF) 基元素类、各种支持 WPF 属性系统和事件逻辑的类以及由 WPF 核心和框架更加广泛使用的其他类型。**   
* Clipboard	    
提供便于将数据传入和传出系统剪贴板的静态方法。   
* MessageBox	   
显示消息框。   

### **System.Windows.Controls Namespace 提供一些类以创建称为控件的元素，从而使用户可使用这些元素与应用程序进行交互。 控件类在用户的所有应用程序体验中处于核心地位，因为用户可使用它们来查看、选择或输入数据或其他信息。**   
* .....................

### **System.Windows.Forms 命名空间包含用于创建基于 Windows 的应用程序的类，以充分利用 Microsoft Windows 操作系统中提供的丰富的用户界面功能。**
* .....................

### **System.Xml 命名空间为处理 XML 提供基于标准的支持。**   
* XmlDocument	   
表示 XML 文档。 可使用此类在文档中加载、验证、编辑、添加和放置 XML。   
* XmlElement	    
表示元素。    
* XmlNode	    
表示 XML 文档中的单个节点。    

### **System.Xml.Linq Namespace 包含 LINQ to XML 的类。 LINQ to XML 是内存中的 XML 编程接口，使您可以轻松有效地修改 XML 文档。**   
* XDocument	    
表示 XML 文档。 有关 XDocument 对象的组件和用法，请参阅 XDocument Class Overview。    
* XNode	    
表示 XML 树中节点的抽象概念（元素、注释、文档类型、处理指令或文本节点）。    

