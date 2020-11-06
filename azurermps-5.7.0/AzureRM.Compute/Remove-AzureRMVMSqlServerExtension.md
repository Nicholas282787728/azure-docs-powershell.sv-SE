---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574350"
---
# <span data-ttu-id="2a5a7-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a5a7-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="2a5a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5a7-103">Tar bort ett SQL Server-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a5a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a5a7-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="2a5a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="2a5a7-106">Cmdleten **Remove-AzureRmVMSqlServerExtension** tar bort ett AzureSQL-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="2a5a7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="2a5a7-108">Exempel 1: ta bort ett SQL Server-tillägg</span><span class="sxs-lookup"><span data-stu-id="2a5a7-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="2a5a7-109">Det här kommandot tar bort ett SQL Server-tillägg från den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="2a5a7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a5a7-110">PARAMETERS</span></span>

### <span data-ttu-id="2a5a7-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a5a7-111">-Name</span></span>
<span data-ttu-id="2a5a7-112">Anger namnet på SQL Server tillägget som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5a7-113">-ResourceGroupName</span></span>
<span data-ttu-id="2a5a7-114">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="2a5a7-115">-VMName</span></span>
<span data-ttu-id="2a5a7-116">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5a7-117">CommonParameters</span></span>
<span data-ttu-id="2a5a7-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5a7-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5a7-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a5a7-120">INPUTS</span></span>

### <span data-ttu-id="2a5a7-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="2a5a7-121">None</span></span>
<span data-ttu-id="2a5a7-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a5a7-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a5a7-123">OUTPUTS</span></span>

## <span data-ttu-id="2a5a7-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a5a7-124">NOTES</span></span>

## <span data-ttu-id="2a5a7-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a5a7-125">RELATED LINKS</span></span>

[<span data-ttu-id="2a5a7-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a5a7-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="2a5a7-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a5a7-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


