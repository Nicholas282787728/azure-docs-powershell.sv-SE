---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574733"
---
# <span data-ttu-id="a7c4d-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a7c4d-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="a7c4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c4d-103">Ändrar tillstånd för en VMSS-instans.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7c4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7c4d-104">SYNTAX</span></span>

### <span data-ttu-id="a7c4d-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="a7c4d-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7c4d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a7c4d-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7c4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7c4d-107">DESCRIPTION</span></span>
<span data-ttu-id="a7c4d-108">Cmdleten **set-AzureRmVmssVM** ändrar tillståndet för en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a7c4d-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a7c4d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7c4d-109">EXAMPLES</span></span>

## <span data-ttu-id="a7c4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7c4d-110">PARAMETERS</span></span>

### <span data-ttu-id="a7c4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c4d-111">-DefaultProfile</span></span>
<span data-ttu-id="a7c4d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7c4d-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a7c4d-113">-InstanceId</span></span>
<span data-ttu-id="a7c4d-114">Anger ID för den VMSS-instans som denna cmdlet ändrar tillstånd för.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c4d-115">-Ombild</span><span class="sxs-lookup"><span data-stu-id="a7c4d-115">-Reimage</span></span>
<span data-ttu-id="a7c4d-116">Anger att denna cmdlet ombildar VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c4d-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="a7c4d-117">-ReimageAll</span></span>
<span data-ttu-id="a7c4d-118">Anger att cmdleten återavbildningar alla diskar i VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7c4d-120">Anger namnet på den resurs grupp som innehåller VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c4d-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a7c4d-121">-VMScaleSetName</span></span>
<span data-ttu-id="a7c4d-122">Anger namnet på den VMSS-instans som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c4d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a7c4d-123">-Confirm</span></span>
<span data-ttu-id="a7c4d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c4d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c4d-125">-WhatIf</span></span>
<span data-ttu-id="a7c4d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7c4d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c4d-128">CommonParameters</span></span>
<span data-ttu-id="a7c4d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c4d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7c4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c4d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7c4d-131">INPUTS</span></span>

## <span data-ttu-id="a7c4d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7c4d-132">OUTPUTS</span></span>

## <span data-ttu-id="a7c4d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7c4d-133">NOTES</span></span>

## <span data-ttu-id="a7c4d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7c4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7c4d-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a7c4d-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
