---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 47e1e33f282cbb238c6bbb53bb007d593b9c043f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574164"
---
# <span data-ttu-id="b7641-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b7641-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="b7641-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7641-102">SYNOPSIS</span></span>
<span data-ttu-id="b7641-103">Ta bort en eller flera tjänst Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="b7641-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7641-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7641-104">SYNTAX</span></span>

### <span data-ttu-id="b7641-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b7641-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7641-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b7641-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7641-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7641-107">DESCRIPTION</span></span>
<span data-ttu-id="b7641-108">Använd **Remove-AzureRmServiceFabricSetting** för att ta bort tjänstens Fabric-inställningar från klustret.</span><span class="sxs-lookup"><span data-stu-id="b7641-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="b7641-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7641-109">EXAMPLES</span></span>

### <span data-ttu-id="b7641-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7641-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="b7641-111">Med det här kommandot tas inställningarna ' MaxCursors ' bort under avsnittet ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="b7641-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="b7641-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7641-112">PARAMETERS</span></span>

### <span data-ttu-id="b7641-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7641-113">-DefaultProfile</span></span>
<span data-ttu-id="b7641-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7641-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7641-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7641-115">-Name</span></span>
<span data-ttu-id="b7641-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="b7641-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b7641-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b7641-117">-Parameter</span></span>
<span data-ttu-id="b7641-118">Indataparametern.</span><span class="sxs-lookup"><span data-stu-id="b7641-118">Parameter.</span></span>

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

### <span data-ttu-id="b7641-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7641-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7641-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b7641-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b7641-121">-Avsnitt</span><span class="sxs-lookup"><span data-stu-id="b7641-121">-Section</span></span>
<span data-ttu-id="b7641-122">Del.</span><span class="sxs-lookup"><span data-stu-id="b7641-122">Section.</span></span>

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

### <span data-ttu-id="b7641-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b7641-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="b7641-124">Typ av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="b7641-124">Client authentication type.</span></span>

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

### <span data-ttu-id="b7641-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7641-125">-Confirm</span></span>
<span data-ttu-id="b7641-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7641-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7641-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7641-127">-WhatIf</span></span>
<span data-ttu-id="b7641-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7641-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7641-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7641-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7641-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7641-130">CommonParameters</span></span>
<span data-ttu-id="b7641-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7641-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7641-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7641-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7641-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7641-133">INPUTS</span></span>

### <span data-ttu-id="b7641-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b7641-134">System.String</span></span>
<span data-ttu-id="b7641-135">Microsoft. Azure. commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="b7641-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b7641-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7641-136">OUTPUTS</span></span>

### <span data-ttu-id="b7641-137">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="b7641-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="b7641-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7641-138">NOTES</span></span>

## <span data-ttu-id="b7641-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7641-139">RELATED LINKS</span></span>

