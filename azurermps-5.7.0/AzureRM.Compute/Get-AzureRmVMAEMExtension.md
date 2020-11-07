---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757712"
---
# <span data-ttu-id="d35a3-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d35a3-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="d35a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d35a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d35a3-103">Hämtar information om AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="d35a3-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d35a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d35a3-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d35a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d35a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d35a3-106">Cmdleten **Get-AzureRmVMAEMExtension** hämtar information om tillägget Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="d35a3-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="d35a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d35a3-107">EXAMPLES</span></span>

### <span data-ttu-id="d35a3-108">Exempel 1: skaffa AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="d35a3-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d35a3-109">Med det här kommandot får du information om AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="d35a3-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d35a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d35a3-110">PARAMETERS</span></span>

### <span data-ttu-id="d35a3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d35a3-111">-Name</span></span>
<span data-ttu-id="d35a3-112">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d35a3-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d35a3-113">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="d35a3-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="d35a3-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="d35a3-114">-OSType</span></span>
<span data-ttu-id="d35a3-115">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="d35a3-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d35a3-116">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="d35a3-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d35a3-117">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="d35a3-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35a3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d35a3-118">-ResourceGroupName</span></span>
<span data-ttu-id="d35a3-119">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d35a3-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="d35a3-120">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d35a3-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="d35a3-121">-Status</span><span class="sxs-lookup"><span data-stu-id="d35a3-121">-Status</span></span>
<span data-ttu-id="d35a3-122">Anger att denna cmdlet endast får instans vyn för AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="d35a3-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d35a3-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d35a3-123">-VMName</span></span>
<span data-ttu-id="d35a3-124">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d35a3-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d35a3-125">Denna cmdlet hämtar information om AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d35a3-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d35a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35a3-126">CommonParameters</span></span>
<span data-ttu-id="d35a3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d35a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35a3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d35a3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35a3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d35a3-129">INPUTS</span></span>

### <span data-ttu-id="d35a3-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="d35a3-130">None</span></span>
<span data-ttu-id="d35a3-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d35a3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d35a3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d35a3-132">OUTPUTS</span></span>

## <span data-ttu-id="d35a3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d35a3-133">NOTES</span></span>

## <span data-ttu-id="d35a3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d35a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="d35a3-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d35a3-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="d35a3-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d35a3-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="d35a3-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d35a3-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


