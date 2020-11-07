---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931026"
---
# <span data-ttu-id="425dd-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="425dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="425dd-102">SYNOPSIS</span></span>
<span data-ttu-id="425dd-103">Startar om VMSS eller en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="425dd-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="425dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="425dd-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="425dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="425dd-105">DESCRIPTION</span></span>
<span data-ttu-id="425dd-106">Cmdleten **restart-AzureRmVmss** startar om den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="425dd-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="425dd-107">Denna cmdlet kan också användas för att starta om en specifik virtuell dator i VMSS med hjälp av *InstanceID* -parametern.</span><span class="sxs-lookup"><span data-stu-id="425dd-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="425dd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="425dd-108">EXAMPLES</span></span>

### <span data-ttu-id="425dd-109">Exempel 1: starta om VMSS</span><span class="sxs-lookup"><span data-stu-id="425dd-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="425dd-110">Det här kommandot startar om VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="425dd-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="425dd-111">Exempel 2: starta om en specifik virtuell dator inom VMSS</span><span class="sxs-lookup"><span data-stu-id="425dd-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="425dd-112">Det här kommandot startar om en virtuell dator som har instans-ID 1 i VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="425dd-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="425dd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="425dd-113">PARAMETERS</span></span>

### <span data-ttu-id="425dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="425dd-114">-AsJob</span></span>
<span data-ttu-id="425dd-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="425dd-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="425dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425dd-116">-DefaultProfile</span></span>
<span data-ttu-id="425dd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="425dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="425dd-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="425dd-118">-InstanceId</span></span>
<span data-ttu-id="425dd-119">Anger ID för de instanser som behöver startas om.</span><span class="sxs-lookup"><span data-stu-id="425dd-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="425dd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="425dd-120">-ResourceGroupName</span></span>
<span data-ttu-id="425dd-121">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="425dd-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="425dd-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="425dd-122">-VMScaleSetName</span></span>
<span data-ttu-id="425dd-123">Arter namnet på den VMSS som denna cmdlet startar om.</span><span class="sxs-lookup"><span data-stu-id="425dd-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="425dd-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="425dd-124">-Confirm</span></span>
<span data-ttu-id="425dd-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="425dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="425dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="425dd-126">-WhatIf</span></span>
<span data-ttu-id="425dd-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="425dd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="425dd-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="425dd-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="425dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425dd-129">CommonParameters</span></span>
<span data-ttu-id="425dd-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425dd-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="425dd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425dd-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="425dd-132">INPUTS</span></span>

### <span data-ttu-id="425dd-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="425dd-133">None</span></span>
<span data-ttu-id="425dd-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="425dd-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="425dd-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="425dd-135">OUTPUTS</span></span>

###  
<span data-ttu-id="425dd-136">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="425dd-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="425dd-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="425dd-137">NOTES</span></span>

## <span data-ttu-id="425dd-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="425dd-138">RELATED LINKS</span></span>

[<span data-ttu-id="425dd-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="425dd-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="425dd-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="425dd-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="425dd-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="425dd-144">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="425dd-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="425dd-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


