---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757998"
---
# <span data-ttu-id="83668-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="83668-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="83668-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83668-102">SYNOPSIS</span></span>
<span data-ttu-id="83668-103">Tar bort en webbplats återställnings Server från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="83668-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83668-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83668-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83668-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83668-105">DESCRIPTION</span></span>
<span data-ttu-id="83668-106">Cmdleten **Remove-AzureRmSiteRecoveryServer** avregistrerar en Azure Site Recovery-server som tar bort den från det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="83668-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="83668-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83668-107">EXAMPLES</span></span>

## <span data-ttu-id="83668-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83668-108">PARAMETERS</span></span>

### <span data-ttu-id="83668-109">-Force</span><span class="sxs-lookup"><span data-stu-id="83668-109">-Force</span></span>
<span data-ttu-id="83668-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="83668-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83668-111">-Server</span><span class="sxs-lookup"><span data-stu-id="83668-111">-Server</span></span>
<span data-ttu-id="83668-112">Anger Site Recovery Server-objekt.</span><span class="sxs-lookup"><span data-stu-id="83668-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83668-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83668-113">-Confirm</span></span>
<span data-ttu-id="83668-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83668-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83668-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83668-115">-WhatIf</span></span>
<span data-ttu-id="83668-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83668-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="83668-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83668-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83668-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83668-118">-DefaultProfile</span></span>
<span data-ttu-id="83668-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83668-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83668-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83668-120">CommonParameters</span></span>
<span data-ttu-id="83668-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83668-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83668-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83668-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83668-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83668-123">INPUTS</span></span>

### <span data-ttu-id="83668-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="83668-124">ASRServer</span></span>
<span data-ttu-id="83668-125">Parametern ' Server ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="83668-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="83668-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83668-126">OUTPUTS</span></span>

### <span data-ttu-id="83668-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="83668-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="83668-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83668-128">NOTES</span></span>

## <span data-ttu-id="83668-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83668-129">RELATED LINKS</span></span>

[<span data-ttu-id="83668-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="83668-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="83668-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="83668-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)