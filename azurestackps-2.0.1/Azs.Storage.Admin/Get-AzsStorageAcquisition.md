---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092987"
---
# <span data-ttu-id="5026e-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="5026e-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="5026e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5026e-102">SYNOPSIS</span></span>
<span data-ttu-id="5026e-103">Returnerar en lista med BLOB-förvärv.</span><span class="sxs-lookup"><span data-stu-id="5026e-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="5026e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5026e-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5026e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5026e-105">DESCRIPTION</span></span>
<span data-ttu-id="5026e-106">Returnerar en lista med BLOB-förvärv.</span><span class="sxs-lookup"><span data-stu-id="5026e-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="5026e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5026e-107">EXAMPLES</span></span>

### <span data-ttu-id="5026e-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="5026e-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="5026e-109">Hämta listan över BLOB-Acquistions.</span><span class="sxs-lookup"><span data-stu-id="5026e-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="5026e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5026e-110">PARAMETERS</span></span>

### <span data-ttu-id="5026e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5026e-111">-DefaultProfile</span></span>
<span data-ttu-id="5026e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5026e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5026e-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="5026e-113">-Location</span></span>
<span data-ttu-id="5026e-114">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="5026e-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5026e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5026e-115">-SubscriptionId</span></span>
<span data-ttu-id="5026e-116">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="5026e-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5026e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5026e-117">CommonParameters</span></span>
<span data-ttu-id="5026e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5026e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5026e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5026e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5026e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5026e-120">INPUTS</span></span>

## <span data-ttu-id="5026e-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5026e-121">OUTPUTS</span></span>

### <span data-ttu-id="5026e-122">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="5026e-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="5026e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5026e-123">NOTES</span></span>

## <span data-ttu-id="5026e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5026e-124">RELATED LINKS</span></span>

