---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: ef369f67e683a214538f1ecb113f771e2f5cd2f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575824"
---
# <span data-ttu-id="901a3-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="901a3-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="901a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="901a3-102">SYNOPSIS</span></span>
<span data-ttu-id="901a3-103">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="901a3-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="901a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="901a3-104">SYNTAX</span></span>

### <span data-ttu-id="901a3-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="901a3-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="901a3-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="901a3-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="901a3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="901a3-107">DESCRIPTION</span></span>
<span data-ttu-id="901a3-108">Använd **set-AzureRmServiceFabricSetting** för att lägga till eller uppdatera tjänstens Fabric-inställningar i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="901a3-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="901a3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="901a3-109">EXAMPLES</span></span>

### <span data-ttu-id="901a3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="901a3-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="901a3-111">Det här kommandot anger ' MaxFileOperationTimeout ' till värdet ' 5000 ' under avsnittet ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="901a3-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="901a3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="901a3-112">PARAMETERS</span></span>

### <span data-ttu-id="901a3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="901a3-113">-Name</span></span>
<span data-ttu-id="901a3-114">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="901a3-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="901a3-115">-Parameter</span><span class="sxs-lookup"><span data-stu-id="901a3-115">-Parameter</span></span>
<span data-ttu-id="901a3-116">Indataparametern.</span><span class="sxs-lookup"><span data-stu-id="901a3-116">Parameter.</span></span>

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

### <span data-ttu-id="901a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="901a3-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="901a3-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="901a3-119">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="901a3-119">-Section</span></span>
<span data-ttu-id="901a3-120">Del.</span><span class="sxs-lookup"><span data-stu-id="901a3-120">Section.</span></span>

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

### <span data-ttu-id="901a3-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="901a3-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="901a3-122">Typ av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="901a3-122">Client authentication type.</span></span>

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

### <span data-ttu-id="901a3-123">-Värde</span><span class="sxs-lookup"><span data-stu-id="901a3-123">-Value</span></span>
<span data-ttu-id="901a3-124">Värdepar.</span><span class="sxs-lookup"><span data-stu-id="901a3-124">Value.</span></span>

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

### <span data-ttu-id="901a3-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="901a3-125">-Confirm</span></span>
<span data-ttu-id="901a3-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="901a3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="901a3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901a3-127">-WhatIf</span></span>
<span data-ttu-id="901a3-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="901a3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="901a3-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="901a3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="901a3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901a3-130">-DefaultProfile</span></span>
<span data-ttu-id="901a3-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="901a3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="901a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901a3-132">CommonParameters</span></span>
<span data-ttu-id="901a3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901a3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901a3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901a3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="901a3-135">INPUTS</span></span>

### <span data-ttu-id="901a3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="901a3-136">System.String</span></span>
<span data-ttu-id="901a3-137">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="901a3-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="901a3-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="901a3-138">OUTPUTS</span></span>

### <span data-ttu-id="901a3-139">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="901a3-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="901a3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="901a3-140">NOTES</span></span>

## <span data-ttu-id="901a3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="901a3-141">RELATED LINKS</span></span>

