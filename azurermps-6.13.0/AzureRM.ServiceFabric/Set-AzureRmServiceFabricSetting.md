---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 42d643faa1b3047c6ee2e3266a68a2ce692ec676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577876"
---
# <span data-ttu-id="e3932-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e3932-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="e3932-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3932-102">SYNOPSIS</span></span>
<span data-ttu-id="e3932-103">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="e3932-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3932-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3932-104">SYNTAX</span></span>

### <span data-ttu-id="e3932-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="e3932-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3932-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="e3932-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3932-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3932-107">DESCRIPTION</span></span>
<span data-ttu-id="e3932-108">Använd **set-AzureRmServiceFabricSetting** för att lägga till eller uppdatera tjänstens Fabric-inställningar i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="e3932-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="e3932-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3932-109">EXAMPLES</span></span>

### <span data-ttu-id="e3932-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3932-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="e3932-111">Det här kommandot anger ' MaxFileOperationTimeout ' till värdet ' 5000 ' under avsnittet ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="e3932-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="e3932-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3932-112">PARAMETERS</span></span>

### <span data-ttu-id="e3932-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3932-113">-DefaultProfile</span></span>
<span data-ttu-id="e3932-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3932-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3932-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3932-115">-Name</span></span>
<span data-ttu-id="e3932-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e3932-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e3932-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e3932-117">-Parameter</span></span>
<span data-ttu-id="e3932-118">Indataparametern.</span><span class="sxs-lookup"><span data-stu-id="e3932-118">Parameter.</span></span>

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

### <span data-ttu-id="e3932-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3932-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3932-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e3932-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e3932-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="e3932-121">-Section</span></span>
<span data-ttu-id="e3932-122">Del.</span><span class="sxs-lookup"><span data-stu-id="e3932-122">Section.</span></span>

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

### <span data-ttu-id="e3932-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="e3932-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="e3932-124">Typ av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="e3932-124">Client authentication type.</span></span>

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

### <span data-ttu-id="e3932-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="e3932-125">-Value</span></span>
<span data-ttu-id="e3932-126">Värdepar.</span><span class="sxs-lookup"><span data-stu-id="e3932-126">Value.</span></span>

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

### <span data-ttu-id="e3932-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3932-127">-Confirm</span></span>
<span data-ttu-id="e3932-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3932-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3932-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3932-129">-WhatIf</span></span>
<span data-ttu-id="e3932-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3932-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3932-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3932-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3932-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3932-132">CommonParameters</span></span>
<span data-ttu-id="e3932-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3932-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3932-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3932-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3932-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3932-135">INPUTS</span></span>

### <span data-ttu-id="e3932-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e3932-136">System.String</span></span>
<span data-ttu-id="e3932-137">Parametrar: parameter (ByValue), section (ByValue), Value (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3932-137">Parameters: Parameter (ByValue), Section (ByValue), Value (ByValue)</span></span>

### <span data-ttu-id="e3932-138">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="e3932-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="e3932-139">Parametrar: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3932-139">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="e3932-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3932-140">OUTPUTS</span></span>

### <span data-ttu-id="e3932-141">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e3932-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e3932-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3932-142">NOTES</span></span>

## <span data-ttu-id="e3932-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3932-143">RELATED LINKS</span></span>
