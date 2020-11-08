---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088895"
---
# <span data-ttu-id="318e3-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="318e3-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="318e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="318e3-102">SYNOPSIS</span></span>
<span data-ttu-id="318e3-103">Hämtar information om konsument inbjudningar.</span><span class="sxs-lookup"><span data-stu-id="318e3-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="318e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="318e3-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="318e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="318e3-105">DESCRIPTION</span></span>
<span data-ttu-id="318e3-106">Cmdleten **Get-AzDataShareReceivedInvitation** innehåller information om alla inbjudningar som klienten har receieved.</span><span class="sxs-lookup"><span data-stu-id="318e3-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="318e3-107">Om du tillhandahåller plats-eller Inbjudnings-ID ger denna cmdlet information om inbjudan, särskilt plats eller efter Inbjudnings-ID. Annars visas en lista med inbjudningar till mottagaren.</span><span class="sxs-lookup"><span data-stu-id="318e3-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="318e3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="318e3-108">EXAMPLES</span></span>

### <span data-ttu-id="318e3-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="318e3-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="318e3-110">Detta ger information om konsument inbjudningar.</span><span class="sxs-lookup"><span data-stu-id="318e3-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="318e3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="318e3-111">PARAMETERS</span></span>

### <span data-ttu-id="318e3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318e3-112">-DefaultProfile</span></span>
<span data-ttu-id="318e3-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="318e3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318e3-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="318e3-114">-InvitationId</span></span>
<span data-ttu-id="318e3-115">Inbjudan-ID för Azure dataShare.</span><span class="sxs-lookup"><span data-stu-id="318e3-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318e3-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="318e3-116">-Location</span></span>
<span data-ttu-id="318e3-117">Plats för inbjudan till Azure Data delning.</span><span class="sxs-lookup"><span data-stu-id="318e3-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318e3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318e3-118">CommonParameters</span></span>
<span data-ttu-id="318e3-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318e3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318e3-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318e3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318e3-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="318e3-121">INPUTS</span></span>

### <span data-ttu-id="318e3-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="318e3-122">None</span></span>

## <span data-ttu-id="318e3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="318e3-123">OUTPUTS</span></span>

### <span data-ttu-id="318e3-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="318e3-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="318e3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="318e3-125">NOTES</span></span>

## <span data-ttu-id="318e3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="318e3-126">RELATED LINKS</span></span>