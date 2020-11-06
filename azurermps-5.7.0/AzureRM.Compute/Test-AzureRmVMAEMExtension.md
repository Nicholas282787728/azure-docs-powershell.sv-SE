---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573509"
---
# <span data-ttu-id="dd51d-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd51d-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="dd51d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd51d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd51d-103">Kontrollerar konfigurationen för AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="dd51d-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd51d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd51d-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="dd51d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd51d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd51d-106">**Testet-AzureRmVMAEMExtension** cmdlet kontrollerar konfigurationen av tillägget Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="dd51d-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="dd51d-107">AEM-tillägget samlar in prestanda data.</span><span class="sxs-lookup"><span data-stu-id="dd51d-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="dd51d-108">Denna cmdlet kontrollerar om prestanda data är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="dd51d-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="dd51d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd51d-109">EXAMPLES</span></span>

### <span data-ttu-id="dd51d-110">Exempel 1: kontrol lera konfigurationen för AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="dd51d-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="dd51d-111">Det här kommandot kontrollerar konfigurationen för AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="dd51d-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="dd51d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd51d-112">PARAMETERS</span></span>

### <span data-ttu-id="dd51d-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="dd51d-113">-OSType</span></span>
<span data-ttu-id="dd51d-114">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="dd51d-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="dd51d-115">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="dd51d-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="dd51d-116">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="dd51d-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd51d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd51d-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd51d-118">Anger namnet på resurs gruppen för den virtuella dator som denna cmdlet kontrollerar.</span><span class="sxs-lookup"><span data-stu-id="dd51d-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="dd51d-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="dd51d-119">-SkipStorageCheck</span></span>
<span data-ttu-id="dd51d-120">Anger att denna cmdlet hoppar över kontrollen av lagrings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd51d-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd51d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="dd51d-121">-VMName</span></span>
<span data-ttu-id="dd51d-122">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dd51d-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dd51d-123">Denna cmdlet testar AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="dd51d-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd51d-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd51d-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="dd51d-125">Anger en tids gräns i minuter för kontroll av lagrings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd51d-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd51d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd51d-126">CommonParameters</span></span>
<span data-ttu-id="dd51d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd51d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd51d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd51d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd51d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd51d-129">INPUTS</span></span>

### <span data-ttu-id="dd51d-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="dd51d-130">None</span></span>
<span data-ttu-id="dd51d-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="dd51d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd51d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd51d-132">OUTPUTS</span></span>

## <span data-ttu-id="dd51d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd51d-133">NOTES</span></span>

## <span data-ttu-id="dd51d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd51d-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd51d-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd51d-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="dd51d-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd51d-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="dd51d-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd51d-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


