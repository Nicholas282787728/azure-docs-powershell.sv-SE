---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a51be31c510d7e428ced0c9ce5ab73a80ab28f75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574200"
---
# <span data-ttu-id="5593e-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5593e-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="5593e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5593e-102">SYNOPSIS</span></span>
<span data-ttu-id="5593e-103">Tar bort den angivna nätverks mappningen för automatisk system återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="5593e-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5593e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5593e-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5593e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5593e-105">DESCRIPTION</span></span>
<span data-ttu-id="5593e-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrNetworkMapping** tar bort den angivna nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="5593e-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="5593e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5593e-107">EXAMPLES</span></span>

### <span data-ttu-id="5593e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5593e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="5593e-109">Tar bort den angivna nätverks mappningen för automatisk återställning och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5593e-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5593e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5593e-110">PARAMETERS</span></span>

### <span data-ttu-id="5593e-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5593e-111">-Confirm</span></span>
<span data-ttu-id="5593e-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5593e-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5593e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5593e-113">-DefaultProfile</span></span>
<span data-ttu-id="5593e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5593e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="5593e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5593e-115">-InputObject</span></span>
<span data-ttu-id="5593e-116">Indatavärdet till cmdlet: det objekt för ASR-nätverket som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="5593e-116">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5593e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5593e-117">-WhatIf</span></span>
<span data-ttu-id="5593e-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5593e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5593e-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5593e-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5593e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5593e-120">CommonParameters</span></span>
<span data-ttu-id="5593e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5593e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5593e-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5593e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5593e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5593e-123">INPUTS</span></span>

### <span data-ttu-id="5593e-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5593e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="5593e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5593e-125">OUTPUTS</span></span>

### <span data-ttu-id="5593e-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5593e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5593e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5593e-127">NOTES</span></span>

## <span data-ttu-id="5593e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5593e-128">RELATED LINKS</span></span>

[<span data-ttu-id="5593e-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5593e-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="5593e-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5593e-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
