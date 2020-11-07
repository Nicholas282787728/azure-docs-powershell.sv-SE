---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 8296945de2bcf98213fc692e486e793a91f84939
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574162"
---
# <span data-ttu-id="9894b-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="9894b-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="9894b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9894b-102">SYNOPSIS</span></span>
<span data-ttu-id="9894b-103">Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.</span><span class="sxs-lookup"><span data-stu-id="9894b-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9894b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9894b-104">SYNTAX</span></span>

### <span data-ttu-id="9894b-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="9894b-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9894b-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="9894b-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9894b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9894b-107">DESCRIPTION</span></span>
<span data-ttu-id="9894b-108">Använd **set-AzureRmServiceFabricSetting** för att lägga till eller uppdatera tjänstens Fabric-inställningar i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="9894b-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="9894b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9894b-109">EXAMPLES</span></span>

### <span data-ttu-id="9894b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9894b-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="9894b-111">Det här kommandot anger ' MaxFileOperationTimeout ' till värdet ' 5000 ' under avsnittet ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="9894b-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="9894b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9894b-112">PARAMETERS</span></span>

### <span data-ttu-id="9894b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9894b-113">-DefaultProfile</span></span>
<span data-ttu-id="9894b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9894b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9894b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9894b-115">-Name</span></span>
<span data-ttu-id="9894b-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="9894b-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9894b-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9894b-117">-Parameter</span></span>
<span data-ttu-id="9894b-118">Indataparametern.</span><span class="sxs-lookup"><span data-stu-id="9894b-118">Parameter.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9894b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9894b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9894b-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9894b-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9894b-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="9894b-121">-Section</span></span>
<span data-ttu-id="9894b-122">Del.</span><span class="sxs-lookup"><span data-stu-id="9894b-122">Section.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9894b-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="9894b-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="9894b-124">Typ av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="9894b-124">Client authentication type.</span></span>

```yaml
Type: PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9894b-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="9894b-125">-Value</span></span>
<span data-ttu-id="9894b-126">Värdepar.</span><span class="sxs-lookup"><span data-stu-id="9894b-126">Value.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9894b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9894b-127">-Confirm</span></span>
<span data-ttu-id="9894b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9894b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9894b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9894b-129">-WhatIf</span></span>
<span data-ttu-id="9894b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9894b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9894b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9894b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9894b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9894b-132">CommonParameters</span></span>
<span data-ttu-id="9894b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9894b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9894b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9894b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9894b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9894b-135">INPUTS</span></span>

### <span data-ttu-id="9894b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9894b-136">System.String</span></span>
<span data-ttu-id="9894b-137">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="9894b-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="9894b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9894b-138">OUTPUTS</span></span>

### <span data-ttu-id="9894b-139">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="9894b-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="9894b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9894b-140">NOTES</span></span>

## <span data-ttu-id="9894b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9894b-141">RELATED LINKS</span></span>
