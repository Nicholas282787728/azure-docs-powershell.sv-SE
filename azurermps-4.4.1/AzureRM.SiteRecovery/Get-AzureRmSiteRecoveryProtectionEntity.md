---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585304"
---
# <span data-ttu-id="9c9f4-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9c9f4-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="9c9f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9f4-103">Hämtar en lista över oskyddade eller skyddade enheter i det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c9f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c9f4-104">SYNTAX</span></span>

### <span data-ttu-id="9c9f4-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9c9f4-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c9f4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9c9f4-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c9f4-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9c9f4-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c9f4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c9f4-108">DESCRIPTION</span></span>
<span data-ttu-id="9c9f4-109">Cmdleten **Get-AzureRmSiteRecoveryProtectionEntity** hämtar en lista över skydds bara eller skyddade enheter, till exempel virtuella datorer, i det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9c9f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c9f4-110">EXAMPLES</span></span>

## <span data-ttu-id="9c9f4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c9f4-111">PARAMETERS</span></span>

### <span data-ttu-id="9c9f4-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9c9f4-112">-FriendlyName</span></span>
<span data-ttu-id="9c9f4-113">Anger det egna namnet på skydds enheten.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9f4-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c9f4-114">-Name</span></span>
<span data-ttu-id="9c9f4-115">Anger namnet på skydds enheten.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-115">Specifies the name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9f4-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9c9f4-116">-ProtectionContainer</span></span>
<span data-ttu-id="9c9f4-117">Anger Protection Container-objekt.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9f4-118">-DefaultProfile</span></span>
<span data-ttu-id="9c9f4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c9f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9f4-120">CommonParameters</span></span>
<span data-ttu-id="9c9f4-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9f4-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c9f4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9f4-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c9f4-123">INPUTS</span></span>

### <span data-ttu-id="9c9f4-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9c9f4-124">ASRProtectionContainer</span></span>
<span data-ttu-id="9c9f4-125">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9c9f4-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="9c9f4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c9f4-126">OUTPUTS</span></span>

### <span data-ttu-id="9c9f4-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="9c9f4-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="9c9f4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c9f4-128">NOTES</span></span>

## <span data-ttu-id="9c9f4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c9f4-129">RELATED LINKS</span></span>

[<span data-ttu-id="9c9f4-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9c9f4-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
