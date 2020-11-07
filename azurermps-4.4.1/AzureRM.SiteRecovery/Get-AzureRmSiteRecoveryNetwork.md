---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575814"
---
# <span data-ttu-id="a91af-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a91af-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="a91af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a91af-102">SYNOPSIS</span></span>
<span data-ttu-id="a91af-103">Hämtar information om nätverken som hanteras av webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="a91af-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a91af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a91af-104">SYNTAX</span></span>

### <span data-ttu-id="a91af-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="a91af-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a91af-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="a91af-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a91af-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="a91af-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a91af-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="a91af-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a91af-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="a91af-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a91af-110">ByName</span><span class="sxs-lookup"><span data-stu-id="a91af-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a91af-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a91af-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a91af-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a91af-112">DESCRIPTION</span></span>
<span data-ttu-id="a91af-113">Cmdleten **Get-AzureRmSiteRecoveryNetwork** hämtar information om Azure Site Recovery-nätverk för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="a91af-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a91af-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a91af-114">EXAMPLES</span></span>

## <span data-ttu-id="a91af-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a91af-115">PARAMETERS</span></span>

### <span data-ttu-id="a91af-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="a91af-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a91af-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a91af-117">-FriendlyName</span></span>
<span data-ttu-id="a91af-118">Anger det egna namnet på den virtuella datorns nätverk.</span><span class="sxs-lookup"><span data-stu-id="a91af-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a91af-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a91af-119">-Name</span></span>
<span data-ttu-id="a91af-120">Anger namnet på den virtuella datorns nätverk.</span><span class="sxs-lookup"><span data-stu-id="a91af-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a91af-121">-Server</span><span class="sxs-lookup"><span data-stu-id="a91af-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a91af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91af-122">-DefaultProfile</span></span>
<span data-ttu-id="a91af-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a91af-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a91af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91af-124">CommonParameters</span></span>
<span data-ttu-id="a91af-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a91af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91af-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91af-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a91af-127">INPUTS</span></span>

### <span data-ttu-id="a91af-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a91af-128">ASRFabric</span></span>
<span data-ttu-id="a91af-129">Parametern ' Fabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a91af-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="a91af-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="a91af-130">String</span></span>
<span data-ttu-id="a91af-131">Parametern ' FriendlyName ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="a91af-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a91af-132">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="a91af-132">String</span></span>
<span data-ttu-id="a91af-133">Parametern ' FriendlyName ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="a91af-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a91af-134">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="a91af-134">String</span></span>
<span data-ttu-id="a91af-135">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="a91af-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a91af-136">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="a91af-136">String</span></span>
<span data-ttu-id="a91af-137">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="a91af-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a91af-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="a91af-138">ASRServer</span></span>
<span data-ttu-id="a91af-139">Parametern ' Server ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a91af-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="a91af-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a91af-140">OUTPUTS</span></span>

### <span data-ttu-id="a91af-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="a91af-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="a91af-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a91af-142">NOTES</span></span>

## <span data-ttu-id="a91af-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a91af-143">RELATED LINKS</span></span>
