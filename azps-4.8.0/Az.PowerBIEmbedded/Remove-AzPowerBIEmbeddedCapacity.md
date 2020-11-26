---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260645"
---
# <span data-ttu-id="a59d6-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a59d6-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a59d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a59d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a59d6-103">Tar bort en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="a59d6-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="a59d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a59d6-104">SYNTAX</span></span>

### <span data-ttu-id="a59d6-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="a59d6-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a59d6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a59d6-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a59d6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a59d6-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a59d6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a59d6-108">DESCRIPTION</span></span>
<span data-ttu-id="a59d6-109">Remove-AzPowerBIEmbeddedCapacity-cmdleten tar bort en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="a59d6-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a59d6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a59d6-110">EXAMPLES</span></span>

### <span data-ttu-id="a59d6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a59d6-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="a59d6-112">Det här kommandot tar bort kapaciteten som heter testcapacity i resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="a59d6-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="a59d6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a59d6-113">PARAMETERS</span></span>

### <span data-ttu-id="a59d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a59d6-114">-DefaultProfile</span></span>
<span data-ttu-id="a59d6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a59d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a59d6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a59d6-116">-InputObject</span></span>
<span data-ttu-id="a59d6-117">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="a59d6-117">Input object for Piping</span></span>

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

### <span data-ttu-id="a59d6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a59d6-118">-Name</span></span>
<span data-ttu-id="a59d6-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="a59d6-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a59d6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a59d6-120">-PassThru</span></span>
<span data-ttu-id="a59d6-121">Returnerar den borttagna kapacitets informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="a59d6-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="a59d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a59d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a59d6-123">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="a59d6-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="a59d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a59d6-124">-ResourceId</span></span>
<span data-ttu-id="a59d6-125">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="a59d6-125">Azure resource ID</span></span>

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

### <span data-ttu-id="a59d6-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a59d6-126">-Confirm</span></span>
<span data-ttu-id="a59d6-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="a59d6-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a59d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a59d6-128">-WhatIf</span></span>
<span data-ttu-id="a59d6-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="a59d6-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a59d6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59d6-130">CommonParameters</span></span>
<span data-ttu-id="a59d6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a59d6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59d6-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a59d6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59d6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a59d6-133">INPUTS</span></span>

### <span data-ttu-id="a59d6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a59d6-134">System.String</span></span>

### <span data-ttu-id="a59d6-135">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a59d6-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a59d6-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a59d6-136">OUTPUTS</span></span>

### <span data-ttu-id="a59d6-137">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a59d6-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a59d6-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a59d6-138">NOTES</span></span>

## <span data-ttu-id="a59d6-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a59d6-139">RELATED LINKS</span></span>

[<span data-ttu-id="a59d6-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a59d6-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a59d6-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a59d6-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)