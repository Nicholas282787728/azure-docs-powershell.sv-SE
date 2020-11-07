---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 851978fafa35d36923adf4dd2c2a6e071c054d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757212"
---
# <span data-ttu-id="40e8c-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="40e8c-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="40e8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="40e8c-103">Hämtar en lista över oskyddade eller skyddade enheter i det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="40e8c-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40e8c-104">SYNTAX</span></span>

### <span data-ttu-id="40e8c-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="40e8c-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40e8c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="40e8c-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40e8c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="40e8c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e8c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40e8c-108">DESCRIPTION</span></span>
<span data-ttu-id="40e8c-109">Cmdleten **Get-AzureRmSiteRecoveryProtectionEntity** hämtar en lista över skydds bara eller skyddade enheter, till exempel virtuella datorer, i det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="40e8c-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="40e8c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40e8c-110">EXAMPLES</span></span>

## <span data-ttu-id="40e8c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40e8c-111">PARAMETERS</span></span>

### <span data-ttu-id="40e8c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e8c-112">-DefaultProfile</span></span>
<span data-ttu-id="40e8c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40e8c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e8c-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="40e8c-114">-FriendlyName</span></span>
<span data-ttu-id="40e8c-115">Anger det egna namnet på skydds enheten.</span><span class="sxs-lookup"><span data-stu-id="40e8c-115">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e8c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="40e8c-116">-Name</span></span>
<span data-ttu-id="40e8c-117">Anger namnet på skydds enheten.</span><span class="sxs-lookup"><span data-stu-id="40e8c-117">Specifies the name of the protection entity.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e8c-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="40e8c-118">-ProtectionContainer</span></span>
<span data-ttu-id="40e8c-119">Anger Protection Container-objekt.</span><span class="sxs-lookup"><span data-stu-id="40e8c-119">Specifies the protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40e8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e8c-120">CommonParameters</span></span>
<span data-ttu-id="40e8c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e8c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e8c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e8c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40e8c-123">INPUTS</span></span>

### <span data-ttu-id="40e8c-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="40e8c-124">ASRProtectionContainer</span></span>
<span data-ttu-id="40e8c-125">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="40e8c-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="40e8c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40e8c-126">OUTPUTS</span></span>

### <span data-ttu-id="40e8c-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="40e8c-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="40e8c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40e8c-128">NOTES</span></span>

## <span data-ttu-id="40e8c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40e8c-129">RELATED LINKS</span></span>

[<span data-ttu-id="40e8c-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="40e8c-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
