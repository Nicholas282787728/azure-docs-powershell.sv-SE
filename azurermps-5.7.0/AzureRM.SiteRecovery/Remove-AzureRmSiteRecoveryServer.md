---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757190"
---
# <span data-ttu-id="3b006-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="3b006-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="3b006-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b006-102">SYNOPSIS</span></span>
<span data-ttu-id="3b006-103">Tar bort en webbplats återställnings Server från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="3b006-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b006-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b006-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b006-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b006-105">DESCRIPTION</span></span>
<span data-ttu-id="3b006-106">Cmdleten **Remove-AzureRmSiteRecoveryServer** avregistrerar en Azure Site Recovery-server som tar bort den från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="3b006-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="3b006-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b006-107">EXAMPLES</span></span>

## <span data-ttu-id="3b006-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b006-108">PARAMETERS</span></span>

### <span data-ttu-id="3b006-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b006-109">-DefaultProfile</span></span>
<span data-ttu-id="3b006-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b006-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b006-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3b006-111">-Force</span></span>
<span data-ttu-id="3b006-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3b006-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b006-113">-Server</span><span class="sxs-lookup"><span data-stu-id="3b006-113">-Server</span></span>
<span data-ttu-id="3b006-114">Anger Site Recovery Server-objekt.</span><span class="sxs-lookup"><span data-stu-id="3b006-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b006-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b006-115">-Confirm</span></span>
<span data-ttu-id="3b006-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b006-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b006-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b006-117">-WhatIf</span></span>
<span data-ttu-id="3b006-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b006-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3b006-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b006-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b006-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b006-120">CommonParameters</span></span>
<span data-ttu-id="3b006-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b006-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b006-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b006-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b006-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b006-123">INPUTS</span></span>

### <span data-ttu-id="3b006-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="3b006-124">ASRServer</span></span>
<span data-ttu-id="3b006-125">Parametern ' Server ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3b006-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="3b006-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b006-126">OUTPUTS</span></span>

### <span data-ttu-id="3b006-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="3b006-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="3b006-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b006-128">NOTES</span></span>

## <span data-ttu-id="3b006-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b006-129">RELATED LINKS</span></span>

[<span data-ttu-id="3b006-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="3b006-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="3b006-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="3b006-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
