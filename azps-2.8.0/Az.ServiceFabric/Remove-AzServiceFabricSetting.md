---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: a7d7f687001677a8d745acf93a77a7e0942a42d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919149"
---
# <span data-ttu-id="b2aa2-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b2aa2-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="b2aa2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="b2aa2-103">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="b2aa2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2aa2-104">SYNTAX</span></span>

### <span data-ttu-id="b2aa2-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b2aa2-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2aa2-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b2aa2-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2aa2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2aa2-107">DESCRIPTION</span></span>
<span data-ttu-id="b2aa2-108">Använd **Remove-AzServiceFabricSetting** för att ta bort tjänstens Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="b2aa2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2aa2-109">EXAMPLES</span></span>

### <span data-ttu-id="b2aa2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2aa2-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="b2aa2-111">Med det här kommandot tas inställningarna ' MaxCursors ' bort under avsnittet ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="b2aa2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2aa2-112">PARAMETERS</span></span>

### <span data-ttu-id="b2aa2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2aa2-113">-DefaultProfile</span></span>
<span data-ttu-id="b2aa2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2aa2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2aa2-115">-Name</span></span>
<span data-ttu-id="b2aa2-116">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="b2aa2-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b2aa2-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b2aa2-117">-Parameter</span></span>
<span data-ttu-id="b2aa2-118">Parameter namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="b2aa2-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="b2aa2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2aa2-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2aa2-120">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b2aa2-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="b2aa2-121">-Section</span></span>
<span data-ttu-id="b2aa2-122">Avsnitts namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="b2aa2-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="b2aa2-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b2aa2-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="b2aa2-124">En matris med Fabric-inställningar</span><span class="sxs-lookup"><span data-stu-id="b2aa2-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="b2aa2-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2aa2-125">-Confirm</span></span>
<span data-ttu-id="b2aa2-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2aa2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2aa2-127">-WhatIf</span></span>
<span data-ttu-id="b2aa2-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2aa2-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2aa2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2aa2-130">CommonParameters</span></span>
<span data-ttu-id="b2aa2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2aa2-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2aa2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2aa2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2aa2-133">INPUTS</span></span>

### <span data-ttu-id="b2aa2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b2aa2-134">System.String</span></span>

### <span data-ttu-id="b2aa2-135">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="b2aa2-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b2aa2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2aa2-136">OUTPUTS</span></span>

### <span data-ttu-id="b2aa2-137">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b2aa2-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b2aa2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2aa2-138">NOTES</span></span>

## <span data-ttu-id="b2aa2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2aa2-139">RELATED LINKS</span></span>
