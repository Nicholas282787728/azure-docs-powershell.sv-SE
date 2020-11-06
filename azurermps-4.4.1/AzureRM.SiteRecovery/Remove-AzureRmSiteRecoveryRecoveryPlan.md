---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577412"
---
# <span data-ttu-id="813b0-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="813b0-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="813b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="813b0-102">SYNOPSIS</span></span>
<span data-ttu-id="813b0-103">Tar bort en plan för webbplats återställning från webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="813b0-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="813b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="813b0-104">SYNTAX</span></span>

### <span data-ttu-id="813b0-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="813b0-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="813b0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="813b0-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="813b0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="813b0-107">DESCRIPTION</span></span>
<span data-ttu-id="813b0-108">Cmdleten **Remove-AzureRmSiteRecoveryRecoveryPlan** tar bort en plan för webbplats återställning från den aktuella Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="813b0-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="813b0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="813b0-109">EXAMPLES</span></span>

### <span data-ttu-id="813b0-110">Exempel 1: ta bort en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="813b0-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="813b0-111">Det första kommandot använder cmdleten Get-AzureRmSiteRecoveryRecoveryPlan för att hämta en plan för webbplats återställning och lagrar den sedan i $RecoveryPlan-variabeln.</span><span class="sxs-lookup"><span data-stu-id="813b0-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="813b0-112">Det andra kommandot tar bort återställnings planen i $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="813b0-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="813b0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="813b0-113">PARAMETERS</span></span>

### <span data-ttu-id="813b0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="813b0-114">-Name</span></span>
<span data-ttu-id="813b0-115">Anger namnet på den återställnings plan som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="813b0-115">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813b0-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="813b0-116">-RecoveryPlan</span></span>
<span data-ttu-id="813b0-117">Anger återställnings planen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="813b0-117">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="813b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813b0-118">-DefaultProfile</span></span>
<span data-ttu-id="813b0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="813b0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="813b0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813b0-120">CommonParameters</span></span>
<span data-ttu-id="813b0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813b0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813b0-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813b0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813b0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="813b0-123">INPUTS</span></span>

### <span data-ttu-id="813b0-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="813b0-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="813b0-125">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="813b0-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="813b0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="813b0-126">OUTPUTS</span></span>

## <span data-ttu-id="813b0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="813b0-127">NOTES</span></span>

## <span data-ttu-id="813b0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="813b0-128">RELATED LINKS</span></span>

[<span data-ttu-id="813b0-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="813b0-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="813b0-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="813b0-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="813b0-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="813b0-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


