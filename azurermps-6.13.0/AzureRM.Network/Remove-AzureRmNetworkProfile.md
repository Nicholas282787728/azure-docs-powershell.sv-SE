---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757566"
---
# <span data-ttu-id="35b61-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35b61-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="35b61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35b61-102">SYNOPSIS</span></span>
<span data-ttu-id="35b61-103">Tar bort en nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="35b61-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35b61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35b61-104">SYNTAX</span></span>

### <span data-ttu-id="35b61-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="35b61-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b61-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b61-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b61-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b61-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b61-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b61-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35b61-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35b61-109">DESCRIPTION</span></span>
<span data-ttu-id="35b61-110">Cmdleten **Remove-AzureRmNetworkProfile** tar bort en nätverks profil om ingen nätverks gränssnitt (som kontrast med en behållare för nätverks gränssnitt **) har** skapats.</span><span class="sxs-lookup"><span data-stu-id="35b61-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="35b61-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35b61-111">EXAMPLES</span></span>

### <span data-ttu-id="35b61-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35b61-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="35b61-113">Då tas nätverks profilen bort med namnet NP1 från resurs gruppen RG1.</span><span class="sxs-lookup"><span data-stu-id="35b61-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="35b61-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35b61-114">PARAMETERS</span></span>

### <span data-ttu-id="35b61-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35b61-115">-AsJob</span></span>
<span data-ttu-id="35b61-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="35b61-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35b61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b61-117">-DefaultProfile</span></span>
<span data-ttu-id="35b61-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35b61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35b61-119">-Force</span><span class="sxs-lookup"><span data-stu-id="35b61-119">-Force</span></span>
<span data-ttu-id="35b61-120">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="35b61-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="35b61-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35b61-121">-InputObject</span></span>
<span data-ttu-id="35b61-122">Nätverks profil objekt.</span><span class="sxs-lookup"><span data-stu-id="35b61-122">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35b61-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="35b61-123">-Name</span></span>
<span data-ttu-id="35b61-124">Namnet på nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="35b61-124">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b61-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35b61-125">-PassThru</span></span>
<span data-ttu-id="35b61-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="35b61-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="35b61-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b61-127">-ResourceGroupName</span></span>
<span data-ttu-id="35b61-128">Namnet på resurs gruppen för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="35b61-128">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b61-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35b61-129">-ResourceId</span></span>
<span data-ttu-id="35b61-130">Resurs-ID för Azure Resource Manager för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="35b61-130">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b61-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35b61-131">-Confirm</span></span>
<span data-ttu-id="35b61-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35b61-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35b61-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b61-133">-WhatIf</span></span>
<span data-ttu-id="35b61-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35b61-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35b61-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35b61-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35b61-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b61-136">CommonParameters</span></span>
<span data-ttu-id="35b61-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b61-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b61-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b61-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b61-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35b61-139">INPUTS</span></span>

### <span data-ttu-id="35b61-140">System. String</span><span class="sxs-lookup"><span data-stu-id="35b61-140">System.String</span></span>

## <span data-ttu-id="35b61-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35b61-141">OUTPUTS</span></span>

### <span data-ttu-id="35b61-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35b61-142">System.Boolean</span></span>

## <span data-ttu-id="35b61-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35b61-143">NOTES</span></span>

## <span data-ttu-id="35b61-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35b61-144">RELATED LINKS</span></span>
