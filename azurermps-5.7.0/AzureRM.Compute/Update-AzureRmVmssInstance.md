---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573494"
---
# <span data-ttu-id="93d59-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="93d59-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="93d59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93d59-102">SYNOPSIS</span></span>
<span data-ttu-id="93d59-103">Startar en manuell uppgradering av VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="93d59-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93d59-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93d59-105">DESCRIPTION</span></span>
<span data-ttu-id="93d59-106">Update-AzureRmVmssInstance cmdlet startar en manuell uppgradering av angiven virtuell dators (VMSS) instans.</span><span class="sxs-lookup"><span data-stu-id="93d59-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="93d59-107">Detta används när uppgraderings principen på VMSS skal uppsättning är inställd på manuell.</span><span class="sxs-lookup"><span data-stu-id="93d59-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="93d59-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93d59-108">EXAMPLES</span></span>

### <span data-ttu-id="93d59-109">Exempel 1: starta en uppgradering av VMSS-instansen</span><span class="sxs-lookup"><span data-stu-id="93d59-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="93d59-110">Det här kommandot startar en uppgradering av VMSS med namnet VMScaleSet001 som har instans-ID 0.</span><span class="sxs-lookup"><span data-stu-id="93d59-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="93d59-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93d59-111">PARAMETERS</span></span>

### <span data-ttu-id="93d59-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="93d59-112">-InstanceId</span></span>
<span data-ttu-id="93d59-113">Anger, som en sträng mat ris, ID eller ID för den instans som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="93d59-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93d59-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d59-114">-ResourceGroupName</span></span>
<span data-ttu-id="93d59-115">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="93d59-115">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93d59-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="93d59-116">-VMScaleSetName</span></span>
<span data-ttu-id="93d59-117">Anger namnet på den VMSS-instans som denna cmdlet uppgraderar.</span><span class="sxs-lookup"><span data-stu-id="93d59-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93d59-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93d59-118">-Confirm</span></span>
<span data-ttu-id="93d59-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93d59-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d59-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d59-120">-WhatIf</span></span>
<span data-ttu-id="93d59-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93d59-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="93d59-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93d59-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d59-123">CommonParameters</span></span>
<span data-ttu-id="93d59-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d59-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d59-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d59-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93d59-126">INPUTS</span></span>

### <span data-ttu-id="93d59-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="93d59-127">None</span></span>
<span data-ttu-id="93d59-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="93d59-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93d59-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93d59-129">OUTPUTS</span></span>

###  
<span data-ttu-id="93d59-130">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="93d59-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="93d59-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93d59-131">NOTES</span></span>

## <span data-ttu-id="93d59-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93d59-132">RELATED LINKS</span></span>

[<span data-ttu-id="93d59-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="93d59-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


