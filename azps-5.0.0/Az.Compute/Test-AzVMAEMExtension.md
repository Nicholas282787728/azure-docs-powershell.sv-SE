---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: ffc22a8937e56537de167046f661ee4b5d262fed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269999"
---
# <span data-ttu-id="8b446-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8b446-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="8b446-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b446-102">SYNOPSIS</span></span>
<span data-ttu-id="8b446-103">Kontrollerar konfigurationen för AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="8b446-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="8b446-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b446-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b446-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b446-105">DESCRIPTION</span></span>
<span data-ttu-id="8b446-106">**Testet-AzVMAEMExtension** cmdlet kontrollerar konfigurationen av tillägget Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="8b446-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="8b446-107">AEM-tillägget samlar in prestanda data.</span><span class="sxs-lookup"><span data-stu-id="8b446-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="8b446-108">Denna cmdlet kontrollerar om prestanda data är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="8b446-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="8b446-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b446-109">EXAMPLES</span></span>

### <span data-ttu-id="8b446-110">Exempel 1: kontrol lera konfigurationen för AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="8b446-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="8b446-111">Det här kommandot kontrollerar konfigurationen för AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="8b446-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="8b446-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b446-112">PARAMETERS</span></span>

### <span data-ttu-id="8b446-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b446-113">-DefaultProfile</span></span>
<span data-ttu-id="8b446-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b446-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="8b446-115">-OSType</span></span>
<span data-ttu-id="8b446-116">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="8b446-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="8b446-117">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="8b446-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="8b446-118">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="8b446-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b446-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b446-120">Anger namnet på resurs gruppen för den virtuella dator som denna cmdlet kontrollerar.</span><span class="sxs-lookup"><span data-stu-id="8b446-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="8b446-121">-SkipStorageCheck</span></span>
<span data-ttu-id="8b446-122">Anger att denna cmdlet hoppar över kontrollen av lagrings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8b446-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b446-123">-VMName</span></span>
<span data-ttu-id="8b446-124">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8b446-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8b446-125">Denna cmdlet testar AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8b446-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="8b446-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="8b446-127">Anger en tids gräns i minuter för kontroll av lagrings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8b446-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b446-128">CommonParameters</span></span>
<span data-ttu-id="8b446-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b446-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b446-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b446-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b446-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b446-131">INPUTS</span></span>

### <span data-ttu-id="8b446-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8b446-132">System.String</span></span>

## <span data-ttu-id="8b446-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b446-133">OUTPUTS</span></span>

### <span data-ttu-id="8b446-134">Microsoft. Azure. commands. Compute. extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="8b446-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="8b446-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b446-135">NOTES</span></span>

## <span data-ttu-id="8b446-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b446-136">RELATED LINKS</span></span>

[<span data-ttu-id="8b446-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8b446-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="8b446-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8b446-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="8b446-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8b446-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


