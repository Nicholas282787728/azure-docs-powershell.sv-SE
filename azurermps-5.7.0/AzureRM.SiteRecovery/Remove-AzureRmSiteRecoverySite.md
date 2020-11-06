---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: a83b4b8ca3dbe415013fe9a858d46cb886ce4b00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573263"
---
# <span data-ttu-id="a2db5-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="a2db5-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="a2db5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2db5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2db5-103">Tar bort en webbplats återställnings webbplats från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="a2db5-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2db5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2db5-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2db5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2db5-105">DESCRIPTION</span></span>
<span data-ttu-id="a2db5-106">Cmdleten **Remove-AzureRmSiteRecoverySite** tar bort en Azure Site Recovery-webbplats från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="a2db5-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="a2db5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2db5-107">EXAMPLES</span></span>

## <span data-ttu-id="a2db5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2db5-108">PARAMETERS</span></span>

### <span data-ttu-id="a2db5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2db5-109">-DefaultProfile</span></span>
<span data-ttu-id="a2db5-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2db5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2db5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a2db5-111">-Force</span></span>
<span data-ttu-id="a2db5-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a2db5-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db5-113">-Site</span><span class="sxs-lookup"><span data-stu-id="a2db5-113">-Site</span></span>
<span data-ttu-id="a2db5-114">Anger plats objekt för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="a2db5-114">Specifies the Site Recovery site object.</span></span>

```yaml
Type: ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2db5-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2db5-115">-Confirm</span></span>
<span data-ttu-id="a2db5-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2db5-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2db5-117">-WhatIf</span></span>
<span data-ttu-id="a2db5-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2db5-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a2db5-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2db5-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2db5-120">CommonParameters</span></span>
<span data-ttu-id="a2db5-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2db5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2db5-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2db5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2db5-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2db5-123">INPUTS</span></span>

### <span data-ttu-id="a2db5-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="a2db5-124">ASRSite</span></span>
<span data-ttu-id="a2db5-125">Parametern ' site ' godkänner värdet av typen ' ASRSite ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a2db5-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="a2db5-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2db5-126">OUTPUTS</span></span>

## <span data-ttu-id="a2db5-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2db5-127">NOTES</span></span>

## <span data-ttu-id="a2db5-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2db5-128">RELATED LINKS</span></span>

[<span data-ttu-id="a2db5-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="a2db5-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="a2db5-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="a2db5-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
