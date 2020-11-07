---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757997"
---
# <span data-ttu-id="90bc7-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90bc7-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="90bc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="90bc7-103">Uppdaterar en återställnings plan i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="90bc7-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90bc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90bc7-104">SYNTAX</span></span>

### <span data-ttu-id="90bc7-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="90bc7-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90bc7-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="90bc7-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90bc7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90bc7-107">DESCRIPTION</span></span>
<span data-ttu-id="90bc7-108">Cmdleten **Update-AzureRmSiteRecoveryRecoveryPlan** uppdaterar en återställnings plan i Azure Site Recovery och publicerar den sedan.</span><span class="sxs-lookup"><span data-stu-id="90bc7-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="90bc7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90bc7-109">EXAMPLES</span></span>

### <span data-ttu-id="90bc7-110">Exempel 1: uppdatera en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="90bc7-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="90bc7-111">Det här kommandot uppdaterar den angivna återställnings planen och publicerar den sedan.</span><span class="sxs-lookup"><span data-stu-id="90bc7-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="90bc7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90bc7-112">PARAMETERS</span></span>

### <span data-ttu-id="90bc7-113">-Path</span><span class="sxs-lookup"><span data-stu-id="90bc7-113">-Path</span></span>
<span data-ttu-id="90bc7-114">Anger sökvägen till återställnings plan filen för återställnings planen som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="90bc7-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bc7-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90bc7-115">-RecoveryPlan</span></span>
<span data-ttu-id="90bc7-116">Anger en återställnings plan som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="90bc7-116">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90bc7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bc7-117">-DefaultProfile</span></span>
<span data-ttu-id="90bc7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90bc7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90bc7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bc7-119">CommonParameters</span></span>
<span data-ttu-id="90bc7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90bc7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bc7-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90bc7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bc7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90bc7-122">INPUTS</span></span>

### <span data-ttu-id="90bc7-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90bc7-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="90bc7-124">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="90bc7-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="90bc7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90bc7-125">OUTPUTS</span></span>

## <span data-ttu-id="90bc7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90bc7-126">NOTES</span></span>

## <span data-ttu-id="90bc7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90bc7-127">RELATED LINKS</span></span>

[<span data-ttu-id="90bc7-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90bc7-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="90bc7-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90bc7-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="90bc7-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90bc7-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


