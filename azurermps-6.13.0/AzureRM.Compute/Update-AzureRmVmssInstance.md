---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: d29bc2c479eb7799784a4e727764dc897fd715af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756208"
---
# <span data-ttu-id="20a6b-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="20a6b-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="20a6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="20a6b-103">Startar en manuell uppgradering av VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="20a6b-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20a6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20a6b-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20a6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="20a6b-106">Update-AzureRmVmssInstance cmdlet startar en manuell uppgradering av angiven virtuell dators (VMSS) instans.</span><span class="sxs-lookup"><span data-stu-id="20a6b-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="20a6b-107">Detta används när uppgraderings principen på VMSS skal uppsättning är inställd på manuell.</span><span class="sxs-lookup"><span data-stu-id="20a6b-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="20a6b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20a6b-108">EXAMPLES</span></span>

### <span data-ttu-id="20a6b-109">Exempel 1: starta en uppgradering av VMSS-instansen</span><span class="sxs-lookup"><span data-stu-id="20a6b-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="20a6b-110">Det här kommandot startar en uppgradering av VMSS med namnet VMScaleSet001 som har instans-ID 0.</span><span class="sxs-lookup"><span data-stu-id="20a6b-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="20a6b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20a6b-111">PARAMETERS</span></span>

### <span data-ttu-id="20a6b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20a6b-112">-AsJob</span></span>
<span data-ttu-id="20a6b-113">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="20a6b-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="20a6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a6b-114">-DefaultProfile</span></span>
<span data-ttu-id="20a6b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20a6b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a6b-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="20a6b-116">-InstanceId</span></span>
<span data-ttu-id="20a6b-117">Anger, som en sträng mat ris, ID eller ID för den instans som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="20a6b-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a6b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a6b-118">-ResourceGroupName</span></span>
<span data-ttu-id="20a6b-119">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="20a6b-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="20a6b-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="20a6b-120">-VMScaleSetName</span></span>
<span data-ttu-id="20a6b-121">Anger namnet på den VMSS-instans som denna cmdlet uppgraderar.</span><span class="sxs-lookup"><span data-stu-id="20a6b-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="20a6b-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20a6b-122">-Confirm</span></span>
<span data-ttu-id="20a6b-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20a6b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a6b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a6b-124">-WhatIf</span></span>
<span data-ttu-id="20a6b-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20a6b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a6b-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20a6b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a6b-127">CommonParameters</span></span>
<span data-ttu-id="20a6b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a6b-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a6b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a6b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20a6b-130">INPUTS</span></span>

### <span data-ttu-id="20a6b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="20a6b-131">System.String</span></span>

### <span data-ttu-id="20a6b-132">System. string []</span><span class="sxs-lookup"><span data-stu-id="20a6b-132">System.String[]</span></span>

## <span data-ttu-id="20a6b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20a6b-133">OUTPUTS</span></span>

### <span data-ttu-id="20a6b-134">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="20a6b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="20a6b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20a6b-135">NOTES</span></span>

## <span data-ttu-id="20a6b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20a6b-136">RELATED LINKS</span></span>

[<span data-ttu-id="20a6b-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="20a6b-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


