---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9d7cfb1b5bdba7d82d42347dad697c5efa764919
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758314"
---
# <span data-ttu-id="a2e68-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a2e68-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="a2e68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2e68-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e68-103">Uppdateringar (uppdatera Server) informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a2e68-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2e68-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e68-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2e68-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e68-106">Cmdleten **Update-AzureRmRecoveryServicesAsrServicesProvider** uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a2e68-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="a2e68-107">Du kan använda denna cmdlet för att utlösa en uppdatering av informationen från Recovery Services-leverantören.</span><span class="sxs-lookup"><span data-stu-id="a2e68-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="a2e68-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2e68-108">EXAMPLES</span></span>

### <span data-ttu-id="a2e68-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2e68-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="a2e68-110">Startar uppdateringen av informationen från den angivna ASR-leverantören och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a2e68-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a2e68-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2e68-111">PARAMETERS</span></span>

### <span data-ttu-id="a2e68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e68-112">-DefaultProfile</span></span>
<span data-ttu-id="a2e68-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2e68-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a2e68-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2e68-114">-InputObject</span></span>
<span data-ttu-id="a2e68-115">Anger vilket ASR Services-objekt som identifierar den server där informationen ska uppdateras (uppdateras).</span><span class="sxs-lookup"><span data-stu-id="a2e68-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="a2e68-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2e68-116">-Confirm</span></span>
<span data-ttu-id="a2e68-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2e68-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e68-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e68-118">-WhatIf</span></span>
<span data-ttu-id="a2e68-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2e68-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2e68-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2e68-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e68-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e68-121">CommonParameters</span></span>
<span data-ttu-id="a2e68-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2e68-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e68-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e68-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e68-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2e68-124">INPUTS</span></span>

### <span data-ttu-id="a2e68-125">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a2e68-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="a2e68-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2e68-126">OUTPUTS</span></span>

### <span data-ttu-id="a2e68-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="a2e68-127">System.Object</span></span>

## <span data-ttu-id="a2e68-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2e68-128">NOTES</span></span>

## <span data-ttu-id="a2e68-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2e68-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2e68-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a2e68-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="a2e68-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a2e68-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
