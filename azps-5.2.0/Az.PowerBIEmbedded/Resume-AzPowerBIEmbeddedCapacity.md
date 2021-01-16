---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417544"
---
# <span data-ttu-id="27027-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="27027-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="27027-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27027-102">SYNOPSIS</span></span>
<span data-ttu-id="27027-103">Återupptar en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="27027-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="27027-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27027-104">SYNTAX</span></span>

### <span data-ttu-id="27027-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="27027-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27027-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27027-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27027-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27027-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27027-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27027-108">DESCRIPTION</span></span>
<span data-ttu-id="27027-109">Resume-AzPowerBIEmbeddedCapacity cmdlet återupptar en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="27027-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="27027-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27027-110">EXAMPLES</span></span>

### <span data-ttu-id="27027-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27027-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="27027-112">Det här kommandot återupptar en pausad kapacitet som heter testcapacity i resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="27027-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="27027-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27027-113">PARAMETERS</span></span>

### <span data-ttu-id="27027-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27027-114">-DefaultProfile</span></span>
<span data-ttu-id="27027-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27027-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27027-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27027-116">-InputObject</span></span>
<span data-ttu-id="27027-117">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="27027-117">Input object for Piping</span></span>

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

### <span data-ttu-id="27027-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="27027-118">-Name</span></span>
<span data-ttu-id="27027-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="27027-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="27027-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27027-120">-PassThru</span></span>
<span data-ttu-id="27027-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="27027-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="27027-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27027-122">-ResourceGroupName</span></span>
<span data-ttu-id="27027-123">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="27027-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="27027-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27027-124">-ResourceId</span></span>
<span data-ttu-id="27027-125">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="27027-125">Azure resource ID</span></span>

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

### <span data-ttu-id="27027-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27027-126">-Confirm</span></span>
<span data-ttu-id="27027-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="27027-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="27027-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27027-128">-WhatIf</span></span>
<span data-ttu-id="27027-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="27027-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="27027-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27027-130">CommonParameters</span></span>
<span data-ttu-id="27027-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27027-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27027-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27027-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27027-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27027-133">INPUTS</span></span>

### <span data-ttu-id="27027-134">System. String</span><span class="sxs-lookup"><span data-stu-id="27027-134">System.String</span></span>

### <span data-ttu-id="27027-135">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="27027-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="27027-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27027-136">OUTPUTS</span></span>

### <span data-ttu-id="27027-137">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="27027-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="27027-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27027-138">NOTES</span></span>

## <span data-ttu-id="27027-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27027-139">RELATED LINKS</span></span>

[<span data-ttu-id="27027-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="27027-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="27027-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="27027-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
