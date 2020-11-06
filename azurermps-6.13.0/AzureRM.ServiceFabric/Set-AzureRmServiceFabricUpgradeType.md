---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: ddab39c3ad575cd46c427c7346fd635217c0dbca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577875"
---
# <span data-ttu-id="372bf-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="372bf-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="372bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="372bf-102">SYNOPSIS</span></span>
<span data-ttu-id="372bf-103">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="372bf-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="372bf-104">SYNTAX</span></span>

### <span data-ttu-id="372bf-105">Versal</span><span class="sxs-lookup"><span data-stu-id="372bf-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372bf-106">Manövrer</span><span class="sxs-lookup"><span data-stu-id="372bf-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372bf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="372bf-107">DESCRIPTION</span></span>
<span data-ttu-id="372bf-108">Använd **set-AzureRmServiceFabricUpgradeType** för att ange uppgraderings typen till automatisk eller manuell med specifik Service Fabric-kod.</span><span class="sxs-lookup"><span data-stu-id="372bf-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="372bf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="372bf-109">EXAMPLES</span></span>

### <span data-ttu-id="372bf-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="372bf-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="372bf-111">Det här kommandot anger kluster uppgraderings läget till automatisk.</span><span class="sxs-lookup"><span data-stu-id="372bf-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="372bf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="372bf-112">PARAMETERS</span></span>

### <span data-ttu-id="372bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372bf-113">-DefaultProfile</span></span>
<span data-ttu-id="372bf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="372bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="372bf-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="372bf-115">-Name</span></span>
<span data-ttu-id="372bf-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="372bf-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="372bf-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="372bf-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372bf-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="372bf-119">-UpgradeMode</span></span>
<span data-ttu-id="372bf-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="372bf-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372bf-121">-Version</span><span class="sxs-lookup"><span data-stu-id="372bf-121">-Version</span></span>
<span data-ttu-id="372bf-122">Kluster kod version.</span><span class="sxs-lookup"><span data-stu-id="372bf-122">Cluster code version.</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372bf-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="372bf-123">-Confirm</span></span>
<span data-ttu-id="372bf-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="372bf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372bf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372bf-125">-WhatIf</span></span>
<span data-ttu-id="372bf-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="372bf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="372bf-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="372bf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372bf-128">CommonParameters</span></span>
<span data-ttu-id="372bf-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372bf-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372bf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372bf-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="372bf-131">INPUTS</span></span>

### <span data-ttu-id="372bf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="372bf-132">System.String</span></span>
<span data-ttu-id="372bf-133">Parametrar: version (ByValue)</span><span class="sxs-lookup"><span data-stu-id="372bf-133">Parameters: Version (ByValue)</span></span>

### <span data-ttu-id="372bf-134">Microsoft. Azure. commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="372bf-134">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="372bf-135">Parametrar: UpgradeMode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="372bf-135">Parameters: UpgradeMode (ByValue)</span></span>

## <span data-ttu-id="372bf-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="372bf-136">OUTPUTS</span></span>

### <span data-ttu-id="372bf-137">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="372bf-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="372bf-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="372bf-138">NOTES</span></span>

## <span data-ttu-id="372bf-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="372bf-139">RELATED LINKS</span></span>
