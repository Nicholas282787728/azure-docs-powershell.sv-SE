---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581268"
---
# <span data-ttu-id="d83c3-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d83c3-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="d83c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d83c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d83c3-103">Tar bort ett valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="d83c3-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d83c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d83c3-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d83c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d83c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d83c3-106">Cmdleten **Remove-AzureRmSiteRecoveryVault** tar bort ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="d83c3-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d83c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d83c3-107">EXAMPLES</span></span>

## <span data-ttu-id="d83c3-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d83c3-108">PARAMETERS</span></span>

### <span data-ttu-id="d83c3-109">-Valv</span><span class="sxs-lookup"><span data-stu-id="d83c3-109">-Vault</span></span>
<span data-ttu-id="d83c3-110">Anger ett valv för Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="d83c3-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d83c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83c3-111">-DefaultProfile</span></span>
<span data-ttu-id="d83c3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d83c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d83c3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83c3-113">CommonParameters</span></span>
<span data-ttu-id="d83c3-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83c3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83c3-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83c3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83c3-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d83c3-116">INPUTS</span></span>

### <span data-ttu-id="d83c3-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="d83c3-117">ASRVault</span></span>
<span data-ttu-id="d83c3-118">Parametern ' valv ' godkänner värdet av typen ' ASRVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d83c3-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="d83c3-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d83c3-119">OUTPUTS</span></span>

## <span data-ttu-id="d83c3-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d83c3-120">NOTES</span></span>

## <span data-ttu-id="d83c3-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d83c3-121">RELATED LINKS</span></span>

[<span data-ttu-id="d83c3-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d83c3-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="d83c3-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d83c3-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
