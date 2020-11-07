---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756546"
---
# <span data-ttu-id="8808f-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8808f-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="8808f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8808f-102">SYNOPSIS</span></span>
<span data-ttu-id="8808f-103">Tar bort en webbplats återställnings webbplats från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="8808f-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8808f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8808f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8808f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8808f-105">DESCRIPTION</span></span>
<span data-ttu-id="8808f-106">Cmdleten **Remove-AzureRmSiteRecoverySite** tar bort en Azure Site Recovery-webbplats från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="8808f-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="8808f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8808f-107">EXAMPLES</span></span>

## <span data-ttu-id="8808f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8808f-108">PARAMETERS</span></span>

### <span data-ttu-id="8808f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="8808f-109">-Force</span></span>
<span data-ttu-id="8808f-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8808f-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8808f-111">-Site</span><span class="sxs-lookup"><span data-stu-id="8808f-111">-Site</span></span>
<span data-ttu-id="8808f-112">Anger plats objekt för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="8808f-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8808f-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8808f-113">-Confirm</span></span>
<span data-ttu-id="8808f-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8808f-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8808f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8808f-115">-WhatIf</span></span>
<span data-ttu-id="8808f-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8808f-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8808f-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8808f-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8808f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8808f-118">-DefaultProfile</span></span>
<span data-ttu-id="8808f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8808f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8808f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8808f-120">CommonParameters</span></span>
<span data-ttu-id="8808f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8808f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8808f-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8808f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8808f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8808f-123">INPUTS</span></span>

### <span data-ttu-id="8808f-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="8808f-124">ASRSite</span></span>
<span data-ttu-id="8808f-125">Parametern ' site ' godkänner värdet av typen ' ASRSite ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8808f-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="8808f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8808f-126">OUTPUTS</span></span>

## <span data-ttu-id="8808f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8808f-127">NOTES</span></span>

## <span data-ttu-id="8808f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8808f-128">RELATED LINKS</span></span>

[<span data-ttu-id="8808f-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8808f-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="8808f-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8808f-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
