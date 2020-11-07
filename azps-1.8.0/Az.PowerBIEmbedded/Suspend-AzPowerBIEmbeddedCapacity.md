---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8a406ebfe6c919dad30e7a394b0b4a4c912cf557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747526"
---
# <span data-ttu-id="edc26-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="edc26-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="edc26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edc26-102">SYNOPSIS</span></span>
<span data-ttu-id="edc26-103">Avbryter instansen av en PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="edc26-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="edc26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edc26-104">SYNTAX</span></span>

### <span data-ttu-id="edc26-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="edc26-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc26-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="edc26-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc26-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edc26-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edc26-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edc26-108">DESCRIPTION</span></span>
<span data-ttu-id="edc26-109">Suspend-AzPowerBIEmbeddedCapacity cmdlet avbryter en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="edc26-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="edc26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edc26-110">EXAMPLES</span></span>

### <span data-ttu-id="edc26-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="edc26-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="edc26-112">Det här kommandot avaktiverar en aktiv kapacitet som heter testcapacity i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="edc26-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="edc26-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edc26-113">PARAMETERS</span></span>

### <span data-ttu-id="edc26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc26-114">-DefaultProfile</span></span>
<span data-ttu-id="edc26-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edc26-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc26-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edc26-116">-InputObject</span></span>
<span data-ttu-id="edc26-117">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="edc26-117">Input object for Piping</span></span>

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

### <span data-ttu-id="edc26-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="edc26-118">-Name</span></span>
<span data-ttu-id="edc26-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="edc26-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="edc26-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edc26-120">-PassThru</span></span>
<span data-ttu-id="edc26-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="edc26-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="edc26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc26-122">-ResourceGroupName</span></span>
<span data-ttu-id="edc26-123">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="edc26-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="edc26-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edc26-124">-ResourceId</span></span>
<span data-ttu-id="edc26-125">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="edc26-125">Azure resource ID</span></span>

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

### <span data-ttu-id="edc26-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="edc26-126">-Confirm</span></span>
<span data-ttu-id="edc26-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="edc26-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="edc26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc26-128">-WhatIf</span></span>
<span data-ttu-id="edc26-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="edc26-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="edc26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc26-130">CommonParameters</span></span>
<span data-ttu-id="edc26-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edc26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc26-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc26-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc26-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edc26-133">INPUTS</span></span>

### <span data-ttu-id="edc26-134">System. String</span><span class="sxs-lookup"><span data-stu-id="edc26-134">System.String</span></span>

### <span data-ttu-id="edc26-135">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="edc26-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="edc26-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edc26-136">OUTPUTS</span></span>

### <span data-ttu-id="edc26-137">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="edc26-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="edc26-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edc26-138">NOTES</span></span>

## <span data-ttu-id="edc26-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edc26-139">RELATED LINKS</span></span>

[<span data-ttu-id="edc26-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="edc26-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="edc26-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="edc26-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

