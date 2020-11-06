---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573232"
---
# <span data-ttu-id="6524b-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6524b-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="6524b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6524b-102">SYNOPSIS</span></span>
<span data-ttu-id="6524b-103">Uppdaterar en återställnings plan i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="6524b-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6524b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6524b-104">SYNTAX</span></span>

### <span data-ttu-id="6524b-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="6524b-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6524b-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6524b-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6524b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6524b-107">DESCRIPTION</span></span>
<span data-ttu-id="6524b-108">Cmdleten **Update-AzureRmSiteRecoveryRecoveryPlan** uppdaterar en återställnings plan i Azure Site Recovery och publicerar den sedan.</span><span class="sxs-lookup"><span data-stu-id="6524b-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="6524b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6524b-109">EXAMPLES</span></span>

### <span data-ttu-id="6524b-110">Exempel 1: uppdatera en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="6524b-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="6524b-111">Det här kommandot uppdaterar den angivna återställnings planen och publicerar den sedan.</span><span class="sxs-lookup"><span data-stu-id="6524b-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="6524b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6524b-112">PARAMETERS</span></span>

### <span data-ttu-id="6524b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6524b-113">-DefaultProfile</span></span>
<span data-ttu-id="6524b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6524b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6524b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6524b-115">-Path</span></span>
<span data-ttu-id="6524b-116">Anger sökvägen till återställnings plan filen för återställnings planen som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="6524b-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6524b-117">-RecoveryPlan</span></span>
<span data-ttu-id="6524b-118">Anger en återställnings plan som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="6524b-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6524b-119">CommonParameters</span></span>
<span data-ttu-id="6524b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6524b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6524b-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6524b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6524b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6524b-122">INPUTS</span></span>

### <span data-ttu-id="6524b-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6524b-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="6524b-124">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6524b-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="6524b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6524b-125">OUTPUTS</span></span>

## <span data-ttu-id="6524b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6524b-126">NOTES</span></span>

## <span data-ttu-id="6524b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6524b-127">RELATED LINKS</span></span>

[<span data-ttu-id="6524b-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6524b-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6524b-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6524b-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6524b-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6524b-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


