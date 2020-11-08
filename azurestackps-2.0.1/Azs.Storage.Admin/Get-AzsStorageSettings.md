---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093008"
---
# <span data-ttu-id="ae348-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="ae348-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="ae348-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae348-102">SYNOPSIS</span></span>
<span data-ttu-id="ae348-103">Returnerar inställningarna för lagringsprovider för lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="ae348-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="ae348-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae348-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae348-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae348-105">DESCRIPTION</span></span>
<span data-ttu-id="ae348-106">Returnerar inställningarna för lagringsprovider för lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="ae348-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="ae348-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae348-107">EXAMPLES</span></span>

### <span data-ttu-id="ae348-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="ae348-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="ae348-109">Hämta lagrings inställningarna.</span><span class="sxs-lookup"><span data-stu-id="ae348-109">Get the storage settings.</span></span>

## <span data-ttu-id="ae348-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae348-110">PARAMETERS</span></span>

### <span data-ttu-id="ae348-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae348-111">-DefaultProfile</span></span>
<span data-ttu-id="ae348-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae348-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae348-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="ae348-113">-Location</span></span>
<span data-ttu-id="ae348-114">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="ae348-114">Resource location.</span></span>

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

### <span data-ttu-id="ae348-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae348-115">-SubscriptionId</span></span>
<span data-ttu-id="ae348-116">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="ae348-116">Subscription Id.</span></span>

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

### <span data-ttu-id="ae348-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae348-117">CommonParameters</span></span>
<span data-ttu-id="ae348-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae348-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae348-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae348-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae348-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae348-120">INPUTS</span></span>

## <span data-ttu-id="ae348-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae348-121">OUTPUTS</span></span>

### <span data-ttu-id="ae348-122">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="ae348-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="ae348-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae348-123">NOTES</span></span>

## <span data-ttu-id="ae348-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae348-124">RELATED LINKS</span></span>

