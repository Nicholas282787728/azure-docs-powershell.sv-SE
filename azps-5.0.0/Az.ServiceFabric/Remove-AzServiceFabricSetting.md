---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269085"
---
# <span data-ttu-id="fc090-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="fc090-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="fc090-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc090-102">SYNOPSIS</span></span>
<span data-ttu-id="fc090-103">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="fc090-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="fc090-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc090-104">SYNTAX</span></span>

### <span data-ttu-id="fc090-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="fc090-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc090-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="fc090-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc090-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc090-107">DESCRIPTION</span></span>
<span data-ttu-id="fc090-108">Använd **Remove-AzServiceFabricSetting** för att ta bort tjänstens Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="fc090-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="fc090-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc090-109">EXAMPLES</span></span>

### <span data-ttu-id="fc090-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc090-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="fc090-111">Med det här kommandot tas inställningarna ' MaxCursors ' bort under avsnittet ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="fc090-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="fc090-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc090-112">PARAMETERS</span></span>

### <span data-ttu-id="fc090-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc090-113">-DefaultProfile</span></span>
<span data-ttu-id="fc090-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc090-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc090-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc090-115">-Name</span></span>
<span data-ttu-id="fc090-116">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="fc090-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fc090-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="fc090-117">-Parameter</span></span>
<span data-ttu-id="fc090-118">Parameter namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="fc090-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc090-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc090-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc090-120">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fc090-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fc090-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="fc090-121">-Section</span></span>
<span data-ttu-id="fc090-122">Avsnitts namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="fc090-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc090-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="fc090-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="fc090-124">En matris med Fabric-inställningar</span><span class="sxs-lookup"><span data-stu-id="fc090-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc090-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc090-125">-Confirm</span></span>
<span data-ttu-id="fc090-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc090-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc090-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc090-127">-WhatIf</span></span>
<span data-ttu-id="fc090-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc090-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc090-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc090-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc090-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc090-130">CommonParameters</span></span>
<span data-ttu-id="fc090-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc090-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc090-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc090-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc090-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc090-133">INPUTS</span></span>

### <span data-ttu-id="fc090-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fc090-134">System.String</span></span>

### <span data-ttu-id="fc090-135">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="fc090-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="fc090-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc090-136">OUTPUTS</span></span>

### <span data-ttu-id="fc090-137">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fc090-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fc090-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc090-138">NOTES</span></span>

## <span data-ttu-id="fc090-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc090-139">RELATED LINKS</span></span>
