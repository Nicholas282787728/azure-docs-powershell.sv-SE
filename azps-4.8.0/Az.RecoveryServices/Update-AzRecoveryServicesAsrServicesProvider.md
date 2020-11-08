---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261966"
---
# <span data-ttu-id="e7ad8-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e7ad8-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="e7ad8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ad8-103">Uppdateringar (uppdatera Server) informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="e7ad8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7ad8-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ad8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ad8-106">Cmdleten **Update-AzRecoveryServicesAsrServicesProvider** uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="e7ad8-107">Du kan använda denna cmdlet för att utlösa en uppdatering av informationen från Recovery Services-leverantören.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="e7ad8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7ad8-108">EXAMPLES</span></span>

### <span data-ttu-id="e7ad8-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7ad8-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="e7ad8-110">Startar uppdateringen av informationen från den angivna ASR-leverantören och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e7ad8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7ad8-111">PARAMETERS</span></span>

### <span data-ttu-id="e7ad8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ad8-112">-DefaultProfile</span></span>
<span data-ttu-id="e7ad8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e7ad8-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7ad8-114">-InputObject</span></span>
<span data-ttu-id="e7ad8-115">Anger vilket ASR Services-objekt som identifierar den server där informationen ska uppdateras (uppdateras).</span><span class="sxs-lookup"><span data-stu-id="e7ad8-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad8-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7ad8-116">-Confirm</span></span>
<span data-ttu-id="e7ad8-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ad8-118">-WhatIf</span></span>
<span data-ttu-id="e7ad8-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7ad8-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ad8-121">CommonParameters</span></span>
<span data-ttu-id="e7ad8-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ad8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ad8-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7ad8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ad8-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7ad8-124">INPUTS</span></span>

### <span data-ttu-id="e7ad8-125">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e7ad8-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="e7ad8-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7ad8-126">OUTPUTS</span></span>

### <span data-ttu-id="e7ad8-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e7ad8-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e7ad8-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7ad8-128">NOTES</span></span>

## <span data-ttu-id="e7ad8-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7ad8-129">RELATED LINKS</span></span>

[<span data-ttu-id="e7ad8-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e7ad8-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="e7ad8-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e7ad8-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
