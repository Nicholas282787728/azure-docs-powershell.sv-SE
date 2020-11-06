---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: ce38334d3ae37864d53830970d895e29755f6687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573231"
---
# <span data-ttu-id="eb0d4-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="eb0d4-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="eb0d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0d4-103">Uppdaterar en återställnings Server för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="eb0d4-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb0d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb0d4-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb0d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="eb0d4-106">Cmdleten **Update-AzureRmSiteRecoveryServer** uppdaterar en Azure Site Recovery-Server.</span><span class="sxs-lookup"><span data-stu-id="eb0d4-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="eb0d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb0d4-107">EXAMPLES</span></span>

## <span data-ttu-id="eb0d4-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb0d4-108">PARAMETERS</span></span>

### <span data-ttu-id="eb0d4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0d4-109">-DefaultProfile</span></span>
<span data-ttu-id="eb0d4-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb0d4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb0d4-111">-Server</span><span class="sxs-lookup"><span data-stu-id="eb0d4-111">-Server</span></span>
<span data-ttu-id="eb0d4-112">Anger den webbplats återställnings server som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="eb0d4-112">Specifies the Site Recovery server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="eb0d4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0d4-113">CommonParameters</span></span>
<span data-ttu-id="eb0d4-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb0d4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0d4-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb0d4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0d4-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb0d4-116">INPUTS</span></span>

### <span data-ttu-id="eb0d4-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="eb0d4-117">ASRServer</span></span>
<span data-ttu-id="eb0d4-118">Parametern ' Server ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="eb0d4-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="eb0d4-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb0d4-119">OUTPUTS</span></span>

## <span data-ttu-id="eb0d4-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb0d4-120">NOTES</span></span>

## <span data-ttu-id="eb0d4-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb0d4-121">RELATED LINKS</span></span>

[<span data-ttu-id="eb0d4-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="eb0d4-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="eb0d4-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="eb0d4-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
