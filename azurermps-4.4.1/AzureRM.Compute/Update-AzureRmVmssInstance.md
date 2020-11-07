---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 1d7655a78ee2abe00b69d485c35b73cee91ee420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755938"
---
# <span data-ttu-id="40a8e-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="40a8e-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="40a8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="40a8e-103">Startar en manuell uppgradering av VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="40a8e-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40a8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40a8e-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40a8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="40a8e-106">Update-AzureRmVmssInstance cmdlet startar en manuell uppgradering av angiven virtuell dators (VMSS) instans.</span><span class="sxs-lookup"><span data-stu-id="40a8e-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="40a8e-107">Detta används när uppgraderings principen på VMSS skal uppsättning är inställd på manuell.</span><span class="sxs-lookup"><span data-stu-id="40a8e-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="40a8e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40a8e-108">EXAMPLES</span></span>

### <span data-ttu-id="40a8e-109">Exempel 1: starta en uppgradering av VMSS-instansen</span><span class="sxs-lookup"><span data-stu-id="40a8e-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="40a8e-110">Det här kommandot startar en uppgradering av VMSS med namnet VMScaleSet001 som har instans-ID 0.</span><span class="sxs-lookup"><span data-stu-id="40a8e-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="40a8e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40a8e-111">PARAMETERS</span></span>

### <span data-ttu-id="40a8e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a8e-112">-DefaultProfile</span></span>
<span data-ttu-id="40a8e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40a8e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40a8e-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="40a8e-114">-InstanceId</span></span>
<span data-ttu-id="40a8e-115">Anger, som en sträng mat ris, ID eller ID för den instans som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="40a8e-115">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="40a8e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40a8e-116">-ResourceGroupName</span></span>
<span data-ttu-id="40a8e-117">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="40a8e-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="40a8e-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="40a8e-118">-VMScaleSetName</span></span>
<span data-ttu-id="40a8e-119">Anger namnet på den VMSS-instans som denna cmdlet uppgraderar.</span><span class="sxs-lookup"><span data-stu-id="40a8e-119">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="40a8e-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40a8e-120">-Confirm</span></span>
<span data-ttu-id="40a8e-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40a8e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40a8e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40a8e-122">-WhatIf</span></span>
<span data-ttu-id="40a8e-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40a8e-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="40a8e-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40a8e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40a8e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a8e-125">CommonParameters</span></span>
<span data-ttu-id="40a8e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a8e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a8e-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40a8e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a8e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40a8e-128">INPUTS</span></span>

## <span data-ttu-id="40a8e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40a8e-129">OUTPUTS</span></span>

###  
<span data-ttu-id="40a8e-130">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="40a8e-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="40a8e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40a8e-131">NOTES</span></span>

## <span data-ttu-id="40a8e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40a8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="40a8e-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="40a8e-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


