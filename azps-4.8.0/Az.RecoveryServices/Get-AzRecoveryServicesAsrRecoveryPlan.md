---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102609"
---
# <span data-ttu-id="333f6-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="333f6-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="333f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="333f6-102">SYNOPSIS</span></span>
<span data-ttu-id="333f6-103">Hämtar en återställnings plan eller alla återställnings planer i Recovery Services-valvet</span><span class="sxs-lookup"><span data-stu-id="333f6-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="333f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="333f6-104">SYNTAX</span></span>

### <span data-ttu-id="333f6-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="333f6-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="333f6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="333f6-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="333f6-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="333f6-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="333f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="333f6-108">DESCRIPTION</span></span>
<span data-ttu-id="333f6-109">Cmdleten **Get-AzRecoveryServicesAsrRecoveryPlan** hämtar detaljerna för den angivna återställnings planen eller alla återhämtnings planer i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="333f6-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="333f6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="333f6-110">EXAMPLES</span></span>

### <span data-ttu-id="333f6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="333f6-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="333f6-112">Hämtar återställnings planen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="333f6-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="333f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="333f6-113">PARAMETERS</span></span>

### <span data-ttu-id="333f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333f6-114">-DefaultProfile</span></span>
<span data-ttu-id="333f6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="333f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="333f6-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="333f6-116">-FriendlyName</span></span>
<span data-ttu-id="333f6-117">Anger det egna namnet på den återställnings plan som ska visas.</span><span class="sxs-lookup"><span data-stu-id="333f6-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333f6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="333f6-118">-Name</span></span>
<span data-ttu-id="333f6-119">Anger namnet på den återställnings plan som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="333f6-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="333f6-120">-Path</span><span class="sxs-lookup"><span data-stu-id="333f6-120">-Path</span></span>
<span data-ttu-id="333f6-121">Anger den fil Sök väg som den här cmdleten sparar JSON-definitionen för.</span><span class="sxs-lookup"><span data-stu-id="333f6-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="333f6-122">JSON-definitionen kan redige ras för att ändra återställnings planen och användas för att uppdatera återställnings planen via Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span><span class="sxs-lookup"><span data-stu-id="333f6-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333f6-123">CommonParameters</span></span>
<span data-ttu-id="333f6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333f6-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="333f6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333f6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="333f6-126">INPUTS</span></span>

### <span data-ttu-id="333f6-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="333f6-127">None</span></span>

## <span data-ttu-id="333f6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="333f6-128">OUTPUTS</span></span>

### <span data-ttu-id="333f6-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="333f6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="333f6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="333f6-130">NOTES</span></span>

## <span data-ttu-id="333f6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="333f6-131">RELATED LINKS</span></span>

[<span data-ttu-id="333f6-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="333f6-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="333f6-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="333f6-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="333f6-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="333f6-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
