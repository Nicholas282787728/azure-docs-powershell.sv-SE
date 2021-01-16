---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412187"
---
# <span data-ttu-id="b9b15-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b9b15-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="b9b15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9b15-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b15-103">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="b9b15-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="b9b15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9b15-104">SYNTAX</span></span>

### <span data-ttu-id="b9b15-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b9b15-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b15-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b9b15-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b15-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9b15-107">DESCRIPTION</span></span>
<span data-ttu-id="b9b15-108">Använd **set-AzServiceFabricSetting** för att lägga till eller uppdatera tjänstens Fabric-inställningar i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="b9b15-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="b9b15-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9b15-109">EXAMPLES</span></span>

### <span data-ttu-id="b9b15-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b9b15-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="b9b15-111">Det här kommandot anger ' MaxFileOperationTimeout ' till värdet ' 5000 ' under avsnittet ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="b9b15-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="b9b15-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b9b15-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="b9b15-113">Med det här kommandot utlöses en uppgradering för att ange flera infrastruktur inställningar med SettingsSectionDescription parameter.</span><span class="sxs-lookup"><span data-stu-id="b9b15-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="b9b15-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9b15-114">PARAMETERS</span></span>

### <span data-ttu-id="b9b15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b15-115">-DefaultProfile</span></span>
<span data-ttu-id="b9b15-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9b15-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9b15-117">-Name</span></span>
<span data-ttu-id="b9b15-118">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="b9b15-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b9b15-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b9b15-119">-Parameter</span></span>
<span data-ttu-id="b9b15-120">Parameter namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="b9b15-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="b9b15-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b15-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9b15-122">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9b15-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b9b15-123">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="b9b15-123">-Section</span></span>
<span data-ttu-id="b9b15-124">Avsnitts namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="b9b15-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="b9b15-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b9b15-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="b9b15-126">En matris med Fabric-inställningar</span><span class="sxs-lookup"><span data-stu-id="b9b15-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="b9b15-127">-Värde</span><span class="sxs-lookup"><span data-stu-id="b9b15-127">-Value</span></span>
<span data-ttu-id="b9b15-128">Parameter värde för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="b9b15-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="b9b15-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9b15-129">-Confirm</span></span>
<span data-ttu-id="b9b15-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9b15-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b15-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b15-131">-WhatIf</span></span>
<span data-ttu-id="b9b15-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9b15-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b15-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9b15-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b15-134">CommonParameters</span></span>
<span data-ttu-id="b9b15-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b15-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9b15-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b15-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9b15-137">INPUTS</span></span>

### <span data-ttu-id="b9b15-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9b15-138">System.String</span></span>

### <span data-ttu-id="b9b15-139">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="b9b15-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b9b15-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9b15-140">OUTPUTS</span></span>

### <span data-ttu-id="b9b15-141">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b9b15-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b9b15-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9b15-142">NOTES</span></span>

## <span data-ttu-id="b9b15-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9b15-143">RELATED LINKS</span></span>
