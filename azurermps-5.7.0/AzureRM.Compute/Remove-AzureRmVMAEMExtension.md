---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576598"
---
# <span data-ttu-id="c28c7-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c28c7-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="c28c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c28c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c28c7-103">Tar bort AEM-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c28c7-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c28c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c28c7-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c28c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c28c7-105">DESCRIPTION</span></span>
<span data-ttu-id="c28c7-106">Cmdleten **Remove-AzureRmVMAEMExtension** tar bort tillägget Azure Enhanced Monitoring (AEM) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c28c7-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="c28c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c28c7-107">EXAMPLES</span></span>

### <span data-ttu-id="c28c7-108">Exempel 1: ta bort AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="c28c7-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="c28c7-109">Det här kommandot tar bort AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="c28c7-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="c28c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c28c7-110">PARAMETERS</span></span>

### <span data-ttu-id="c28c7-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="c28c7-111">-Name</span></span>
<span data-ttu-id="c28c7-112">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="c28c7-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28c7-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="c28c7-113">-OSType</span></span>
<span data-ttu-id="c28c7-114">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="c28c7-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c28c7-115">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="c28c7-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c28c7-116">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="c28c7-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c28c7-118">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c28c7-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="c28c7-119">Denna cmdlet tar bort AEM-tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c28c7-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="c28c7-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="c28c7-120">-VMName</span></span>
<span data-ttu-id="c28c7-121">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c28c7-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c28c7-122">Denna cmdlet tar bort AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c28c7-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c28c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28c7-123">CommonParameters</span></span>
<span data-ttu-id="c28c7-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28c7-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c28c7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28c7-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c28c7-126">INPUTS</span></span>

### <span data-ttu-id="c28c7-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="c28c7-127">None</span></span>
<span data-ttu-id="c28c7-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c28c7-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c28c7-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c28c7-129">OUTPUTS</span></span>

## <span data-ttu-id="c28c7-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c28c7-130">NOTES</span></span>

## <span data-ttu-id="c28c7-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c28c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="c28c7-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c28c7-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c28c7-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c28c7-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c28c7-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c28c7-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


