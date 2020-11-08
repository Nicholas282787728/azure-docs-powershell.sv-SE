---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 10c9c634d1435e9460b72bfd1ccdb7e77f7fea53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088321"
---
# <span data-ttu-id="4bce9-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="4bce9-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="4bce9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bce9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bce9-103">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="4bce9-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="4bce9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bce9-104">SYNTAX</span></span>

### <span data-ttu-id="4bce9-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="4bce9-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bce9-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="4bce9-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bce9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bce9-107">DESCRIPTION</span></span>
<span data-ttu-id="4bce9-108">Använd **set-AzServiceFabricSetting** för att lägga till eller uppdatera tjänstens Fabric-inställningar i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="4bce9-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="4bce9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bce9-109">EXAMPLES</span></span>

### <span data-ttu-id="4bce9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4bce9-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="4bce9-111">Det här kommandot anger ' MaxFileOperationTimeout ' till värdet ' 5000 ' under avsnittet ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="4bce9-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="4bce9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bce9-112">PARAMETERS</span></span>

### <span data-ttu-id="4bce9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bce9-113">-DefaultProfile</span></span>
<span data-ttu-id="4bce9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bce9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bce9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4bce9-115">-Name</span></span>
<span data-ttu-id="4bce9-116">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="4bce9-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4bce9-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4bce9-117">-Parameter</span></span>
<span data-ttu-id="4bce9-118">Parameter namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="4bce9-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="4bce9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bce9-119">-ResourceGroupName</span></span>
<span data-ttu-id="4bce9-120">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4bce9-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4bce9-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="4bce9-121">-Section</span></span>
<span data-ttu-id="4bce9-122">Avsnitts namn för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="4bce9-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="4bce9-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="4bce9-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="4bce9-124">En matris med Fabric-inställningar</span><span class="sxs-lookup"><span data-stu-id="4bce9-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="4bce9-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="4bce9-125">-Value</span></span>
<span data-ttu-id="4bce9-126">Parameter värde för Fabric-inställningen</span><span class="sxs-lookup"><span data-stu-id="4bce9-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="4bce9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bce9-127">-Confirm</span></span>
<span data-ttu-id="4bce9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bce9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bce9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bce9-129">-WhatIf</span></span>
<span data-ttu-id="4bce9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bce9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bce9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bce9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bce9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bce9-132">CommonParameters</span></span>
<span data-ttu-id="4bce9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bce9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bce9-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bce9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bce9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bce9-135">INPUTS</span></span>

### <span data-ttu-id="4bce9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4bce9-136">System.String</span></span>

### <span data-ttu-id="4bce9-137">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="4bce9-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="4bce9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bce9-138">OUTPUTS</span></span>

### <span data-ttu-id="4bce9-139">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4bce9-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4bce9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bce9-140">NOTES</span></span>

## <span data-ttu-id="4bce9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bce9-141">RELATED LINKS</span></span>
