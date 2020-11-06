---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582995"
---
# <span data-ttu-id="322f4-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="322f4-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="322f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="322f4-102">SYNOPSIS</span></span>
<span data-ttu-id="322f4-103">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="322f4-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="322f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="322f4-104">SYNTAX</span></span>

### <span data-ttu-id="322f4-105">Versal</span><span class="sxs-lookup"><span data-stu-id="322f4-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="322f4-106">Manövrer</span><span class="sxs-lookup"><span data-stu-id="322f4-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="322f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="322f4-107">DESCRIPTION</span></span>
<span data-ttu-id="322f4-108">Använd **set-AzureRmServiceFabricUpgradeType** för att ange uppgraderings typen till automatisk eller manuell med specifik Service Fabric-kod.</span><span class="sxs-lookup"><span data-stu-id="322f4-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="322f4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="322f4-109">EXAMPLES</span></span>

### <span data-ttu-id="322f4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="322f4-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="322f4-111">Det här kommandot anger kluster uppgraderings läget till automatisk.</span><span class="sxs-lookup"><span data-stu-id="322f4-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="322f4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="322f4-112">PARAMETERS</span></span>

### <span data-ttu-id="322f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322f4-113">-DefaultProfile</span></span>
<span data-ttu-id="322f4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="322f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="322f4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="322f4-115">-Name</span></span>
<span data-ttu-id="322f4-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="322f4-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="322f4-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="322f4-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322f4-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="322f4-119">-UpgradeMode</span></span>
<span data-ttu-id="322f4-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="322f4-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="322f4-121">-Version</span><span class="sxs-lookup"><span data-stu-id="322f4-121">-Version</span></span>
<span data-ttu-id="322f4-122">Kluster kod version.</span><span class="sxs-lookup"><span data-stu-id="322f4-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="322f4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="322f4-123">-Confirm</span></span>
<span data-ttu-id="322f4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="322f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="322f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="322f4-125">-WhatIf</span></span>
<span data-ttu-id="322f4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="322f4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="322f4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="322f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="322f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322f4-128">CommonParameters</span></span>
<span data-ttu-id="322f4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="322f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322f4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322f4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="322f4-131">INPUTS</span></span>

### <span data-ttu-id="322f4-132">Microsoft. Azure. commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="322f4-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="322f4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="322f4-133">System.String</span></span>

## <span data-ttu-id="322f4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="322f4-134">OUTPUTS</span></span>

### <span data-ttu-id="322f4-135">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="322f4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="322f4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="322f4-136">NOTES</span></span>

## <span data-ttu-id="322f4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="322f4-137">RELATED LINKS</span></span>

