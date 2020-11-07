---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
ms.openlocfilehash: 07b068587848bc8af92fc49b039155c0a2c4fdd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930617"
---
# <span data-ttu-id="442a7-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="442a7-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="442a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="442a7-102">SYNOPSIS</span></span>
<span data-ttu-id="442a7-103">Startar en manuell uppgradering av VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="442a7-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="442a7-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="442a7-105">DESCRIPTION</span></span>
<span data-ttu-id="442a7-106">Update-AzureRmVmssInstance cmdlet startar en manuell uppgradering av angiven virtuell dators (VMSS) instans.</span><span class="sxs-lookup"><span data-stu-id="442a7-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="442a7-107">Detta används när uppgraderings principen på VMSS skal uppsättning är inställd på manuell.</span><span class="sxs-lookup"><span data-stu-id="442a7-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="442a7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="442a7-108">EXAMPLES</span></span>

### <span data-ttu-id="442a7-109">Exempel 1: starta en uppgradering av VMSS-instansen</span><span class="sxs-lookup"><span data-stu-id="442a7-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="442a7-110">Det här kommandot startar en uppgradering av VMSS med namnet VMScaleSet001 som har instans-ID 0.</span><span class="sxs-lookup"><span data-stu-id="442a7-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="442a7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="442a7-111">PARAMETERS</span></span>

### <span data-ttu-id="442a7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="442a7-112">-AsJob</span></span>
<span data-ttu-id="442a7-113">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="442a7-113">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442a7-114">-DefaultProfile</span></span>
<span data-ttu-id="442a7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="442a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a7-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="442a7-116">-InstanceId</span></span>
<span data-ttu-id="442a7-117">Anger, som en sträng mat ris, ID eller ID för den instans som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="442a7-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="442a7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442a7-118">-ResourceGroupName</span></span>
<span data-ttu-id="442a7-119">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="442a7-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="442a7-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="442a7-120">-VMScaleSetName</span></span>
<span data-ttu-id="442a7-121">Anger namnet på den VMSS-instans som denna cmdlet uppgraderar.</span><span class="sxs-lookup"><span data-stu-id="442a7-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="442a7-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="442a7-122">-Confirm</span></span>
<span data-ttu-id="442a7-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="442a7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442a7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442a7-124">-WhatIf</span></span>
<span data-ttu-id="442a7-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="442a7-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="442a7-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="442a7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442a7-127">CommonParameters</span></span>
<span data-ttu-id="442a7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442a7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442a7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442a7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="442a7-130">INPUTS</span></span>

### <span data-ttu-id="442a7-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="442a7-131">None</span></span>
<span data-ttu-id="442a7-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="442a7-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="442a7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="442a7-133">OUTPUTS</span></span>

###  
<span data-ttu-id="442a7-134">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="442a7-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="442a7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="442a7-135">NOTES</span></span>

## <span data-ttu-id="442a7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="442a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="442a7-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="442a7-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


