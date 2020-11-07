---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c95019c253a4ecb6c442c9f88262f536c4590a83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755818"
---
# <span data-ttu-id="36a2e-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36a2e-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="36a2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="36a2e-103">Avbryter instansen av en PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="36a2e-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36a2e-104">SYNTAX</span></span>

### <span data-ttu-id="36a2e-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="36a2e-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36a2e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36a2e-106">ByResourceId</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36a2e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36a2e-107">ByInputObject</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a2e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36a2e-108">DESCRIPTION</span></span>
<span data-ttu-id="36a2e-109">Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet avbryter en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="36a2e-109">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="36a2e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36a2e-110">EXAMPLES</span></span>

### <span data-ttu-id="36a2e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36a2e-111">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="36a2e-112">Det här kommandot avaktiverar en aktiv kapacitet som heter testcapacity i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="36a2e-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="36a2e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36a2e-113">PARAMETERS</span></span>

### <span data-ttu-id="36a2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a2e-114">-DefaultProfile</span></span>
<span data-ttu-id="36a2e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36a2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36a2e-116">-InputObject</span></span>
<span data-ttu-id="36a2e-117">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="36a2e-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="36a2e-118">-Name</span></span>
<span data-ttu-id="36a2e-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="36a2e-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36a2e-120">-PassThru</span></span>
<span data-ttu-id="36a2e-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="36a2e-121">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="36a2e-123">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="36a2e-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36a2e-124">-ResourceId</span></span>
<span data-ttu-id="36a2e-125">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="36a2e-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36a2e-126">-Confirm</span></span>
<span data-ttu-id="36a2e-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="36a2e-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a2e-128">-WhatIf</span></span>
<span data-ttu-id="36a2e-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="36a2e-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a2e-130">CommonParameters</span></span>
<span data-ttu-id="36a2e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a2e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a2e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a2e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36a2e-133">INPUTS</span></span>

### <span data-ttu-id="36a2e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="36a2e-134">System.String</span></span>

### <span data-ttu-id="36a2e-135">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36a2e-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="36a2e-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36a2e-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="36a2e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36a2e-137">OUTPUTS</span></span>

### <span data-ttu-id="36a2e-138">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36a2e-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="36a2e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36a2e-139">NOTES</span></span>

## <span data-ttu-id="36a2e-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36a2e-140">RELATED LINKS</span></span>

[<span data-ttu-id="36a2e-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36a2e-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="36a2e-142">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36a2e-142">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

