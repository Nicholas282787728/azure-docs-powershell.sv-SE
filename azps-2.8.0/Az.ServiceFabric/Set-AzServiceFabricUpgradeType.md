---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 9eba21106e5e2e7c22045d9aecdb86926e7e8ed7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919145"
---
# <span data-ttu-id="a573a-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a573a-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="a573a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a573a-102">SYNOPSIS</span></span>
<span data-ttu-id="a573a-103">Ändra kluster för Service Fabric-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="a573a-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="a573a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a573a-104">SYNTAX</span></span>

### <span data-ttu-id="a573a-105">Versal</span><span class="sxs-lookup"><span data-stu-id="a573a-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a573a-106">Manövrer</span><span class="sxs-lookup"><span data-stu-id="a573a-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a573a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a573a-107">DESCRIPTION</span></span>
<span data-ttu-id="a573a-108">Använd **set-AzServiceFabricUpgradeType** för att ange uppgraderings typen till automatisk eller manuell med specifik Service Fabric-kod.</span><span class="sxs-lookup"><span data-stu-id="a573a-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="a573a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a573a-109">EXAMPLES</span></span>

### <span data-ttu-id="a573a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a573a-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="a573a-111">Det här kommandot anger kluster uppgraderings läget till automatisk.</span><span class="sxs-lookup"><span data-stu-id="a573a-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="a573a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a573a-112">PARAMETERS</span></span>

### <span data-ttu-id="a573a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a573a-113">-DefaultProfile</span></span>
<span data-ttu-id="a573a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a573a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a573a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a573a-115">-Name</span></span>
<span data-ttu-id="a573a-116">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="a573a-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a573a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a573a-117">-ResourceGroupName</span></span>
<span data-ttu-id="a573a-118">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a573a-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a573a-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a573a-119">-UpgradeMode</span></span>
<span data-ttu-id="a573a-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a573a-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="a573a-121">-Version</span><span class="sxs-lookup"><span data-stu-id="a573a-121">-Version</span></span>
<span data-ttu-id="a573a-122">Kluster kod version</span><span class="sxs-lookup"><span data-stu-id="a573a-122">Cluster code version</span></span>

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

### <span data-ttu-id="a573a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a573a-123">-Confirm</span></span>
<span data-ttu-id="a573a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a573a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a573a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a573a-125">-WhatIf</span></span>
<span data-ttu-id="a573a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a573a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a573a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a573a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a573a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a573a-128">CommonParameters</span></span>
<span data-ttu-id="a573a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a573a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a573a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a573a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a573a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a573a-131">INPUTS</span></span>

### <span data-ttu-id="a573a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a573a-132">System.String</span></span>

### <span data-ttu-id="a573a-133">Microsoft. Azure. commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a573a-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="a573a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a573a-134">OUTPUTS</span></span>

### <span data-ttu-id="a573a-135">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a573a-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a573a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a573a-136">NOTES</span></span>

## <span data-ttu-id="a573a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a573a-137">RELATED LINKS</span></span>
