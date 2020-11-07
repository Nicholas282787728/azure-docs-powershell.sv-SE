---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: cea8ec21021725bae99ef597a33079621f539cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746829"
---
# <span data-ttu-id="2c4d0-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2c4d0-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="2c4d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4d0-103">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="2c4d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c4d0-104">SYNTAX</span></span>

### <span data-ttu-id="2c4d0-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="2c4d0-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4d0-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="2c4d0-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c4d0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c4d0-107">DESCRIPTION</span></span>
<span data-ttu-id="2c4d0-108">Använd **set-AzServiceFabricSetting** för att lägga till eller uppdatera tjänstens Fabric-inställningar i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="2c4d0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c4d0-109">EXAMPLES</span></span>

### <span data-ttu-id="2c4d0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2c4d0-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="2c4d0-111">Det här kommandot anger ' MaxFileOperationTimeout ' till värdet ' 5000 ' under avsnittet ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="2c4d0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c4d0-112">PARAMETERS</span></span>

### <span data-ttu-id="2c4d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4d0-113">-DefaultProfile</span></span>
<span data-ttu-id="2c4d0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c4d0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c4d0-115">-Name</span></span>
<span data-ttu-id="2c4d0-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2c4d0-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2c4d0-117">-Parameter</span></span>
<span data-ttu-id="2c4d0-118">Indataparametern.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-118">Parameter.</span></span>

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

### <span data-ttu-id="2c4d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c4d0-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c4d0-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="2c4d0-121">-Section</span></span>
<span data-ttu-id="2c4d0-122">Del.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-122">Section.</span></span>

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

### <span data-ttu-id="2c4d0-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="2c4d0-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="2c4d0-124">Typ av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-124">Client authentication type.</span></span>

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

### <span data-ttu-id="2c4d0-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="2c4d0-125">-Value</span></span>
<span data-ttu-id="2c4d0-126">Värdepar.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-126">Value.</span></span>

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

### <span data-ttu-id="2c4d0-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c4d0-127">-Confirm</span></span>
<span data-ttu-id="2c4d0-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4d0-129">-WhatIf</span></span>
<span data-ttu-id="2c4d0-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c4d0-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4d0-132">CommonParameters</span></span>
<span data-ttu-id="2c4d0-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4d0-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4d0-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c4d0-135">INPUTS</span></span>

### <span data-ttu-id="2c4d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2c4d0-136">System.String</span></span>

### <span data-ttu-id="2c4d0-137">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="2c4d0-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="2c4d0-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c4d0-138">OUTPUTS</span></span>

### <span data-ttu-id="2c4d0-139">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2c4d0-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2c4d0-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c4d0-140">NOTES</span></span>

## <span data-ttu-id="2c4d0-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c4d0-141">RELATED LINKS</span></span>
