---
title: 泛型类型参数（C# 编程指南）
ms.date: 07/20/2015
helpviewer_keywords:
- generics [C#], type parameters
- type parameters [C#]
ms.assetid: a03b0ab2-0606-4b41-b7bf-e64d5bb4d18f
ms.openlocfilehash: 35029b90fb7b905a87055596cf8dcd6a84ef9d36
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33332463"
---
# <a name="generic-type-parameters-c-programming-guide"></a>泛型类型参数（C# 编程指南）
在泛型类型或方法定义中，类型参数是在其实例化泛型类型的一个变量时，客户端指定的特定类型的占位符。 泛型类（例如[泛型介绍](../../../csharp/programming-guide/generics/introduction-to-generics.md)中列出的 `GenericList<T>`）无法按原样使用，因为它不是真正的类型；它更像是类型的蓝图。 若要使用 `GenericList<T>`，客户端代码必须通过指定尖括号内的类型参数来声明并实例化构造类型。 此特定类的类型参数可以是编译器可识别的任何类型。 可创建任意数量的构造类型实例，其中每个使用不同的类型参数，如下所示：  
  
 [!code-csharp[csProgGuideGenerics#7](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_1.cs)]  
  
 在 `GenericList<T>` 的每个实例中，类中出现的每个 `T` 在运行时均会被替换为类型参数。 通过这种替换，我们已通过使用单个类定义创建了三个单独的类型安全的有效对象。 有关 CLR 如何执行此替换的详细信息，请参阅[运行时中的泛型](../../../csharp/programming-guide/generics/generics-in-the-run-time.md)。  
  
## <a name="type-parameter-naming-guidelines"></a>类型参数命名指南  
  
-   请使用描述性名称命名泛型类型参数，除非单个字母名称完全具有自我说明性且描述性名称不会增加任何作用。  
  
     [!code-csharp[csProgGuideGenerics#8](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_2.cs)]  
  
-   对具有单个字母类型参数的类型，考虑使用 T 作为类型参数名称。  
  
     [!code-csharp[csProgGuideGenerics#9](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_3.cs)]  
  
-   在类型参数描述性名称前添加前缀 "T"。  
  
     [!code-csharp[csProgGuideGenerics#10](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_4.cs)]  
  
-   请考虑在参数名称中指示出类型参数的约束。 例如，约束为 `ISession` 的参数可命名为 `TSession`。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Collections.Generic>  
 [C# 编程指南](../../../csharp/programming-guide/index.md)  
 [泛型](../../../csharp/programming-guide/generics/index.md)  
 [C++ 模板和 C# 泛型之间的区别](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)
