---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575567"
---
# <span data-ttu-id="02a72-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="02a72-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="02a72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02a72-102">SYNOPSIS</span></span>
<span data-ttu-id="02a72-103">Hämtar en återställnings plan eller alla återställnings planer i Recovery Services-valvet</span><span class="sxs-lookup"><span data-stu-id="02a72-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02a72-104">SYNTAX</span></span>

### <span data-ttu-id="02a72-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="02a72-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a72-106">ByName</span><span class="sxs-lookup"><span data-stu-id="02a72-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a72-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="02a72-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a72-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02a72-108">DESCRIPTION</span></span>
<span data-ttu-id="02a72-109">Cmdleten **Get-AzureRmRecoveryServicesAsrRecoveryPlan** hämtar detaljerna för den angivna återställnings planen eller alla återhämtnings planer i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="02a72-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="02a72-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02a72-110">EXAMPLES</span></span>

### <span data-ttu-id="02a72-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02a72-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="02a72-112">Hämtar återställnings planen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="02a72-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="02a72-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02a72-113">PARAMETERS</span></span>

### <span data-ttu-id="02a72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a72-114">-DefaultProfile</span></span>
<span data-ttu-id="02a72-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02a72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="02a72-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="02a72-116">-FriendlyName</span></span>
<span data-ttu-id="02a72-117">Anger det egna namnet på den återställnings plan som ska visas.</span><span class="sxs-lookup"><span data-stu-id="02a72-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a72-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="02a72-118">-Name</span></span>
<span data-ttu-id="02a72-119">Anger namnet på den återställnings plan som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="02a72-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a72-120">-Path</span><span class="sxs-lookup"><span data-stu-id="02a72-120">-Path</span></span>
<span data-ttu-id="02a72-121">Anger den fil Sök väg som den här cmdleten sparar JSON-definitionen för.</span><span class="sxs-lookup"><span data-stu-id="02a72-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="02a72-122">JSON-definitionen kan redige ras för att ändra återställnings planen och användas för att uppdatera återställnings planen via Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span><span class="sxs-lookup"><span data-stu-id="02a72-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a72-123">CommonParameters</span></span>
<span data-ttu-id="02a72-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a72-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a72-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02a72-126">INPUTS</span></span>

### <span data-ttu-id="02a72-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="02a72-127">None</span></span>

## <span data-ttu-id="02a72-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02a72-128">OUTPUTS</span></span>

### <span data-ttu-id="02a72-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="02a72-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="02a72-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02a72-130">NOTES</span></span>

## <span data-ttu-id="02a72-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02a72-131">RELATED LINKS</span></span>

[<span data-ttu-id="02a72-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="02a72-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="02a72-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="02a72-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="02a72-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="02a72-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
