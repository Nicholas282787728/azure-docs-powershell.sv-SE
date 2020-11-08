---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100197"
---
# <span data-ttu-id="46c1a-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="46c1a-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="46c1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="46c1a-103">Lista över offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="46c1a-103">List of public ip addresses.</span></span>

## <span data-ttu-id="46c1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46c1a-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="46c1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="46c1a-106">Lista över offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="46c1a-106">List of public ip addresses.</span></span>

## <span data-ttu-id="46c1a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="46c1a-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46c1a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="46c1a-109">Hämta listan med offentliga IP-adresser, antingen tilldelade eller inte tilldelade.</span><span class="sxs-lookup"><span data-stu-id="46c1a-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="46c1a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46c1a-110">PARAMETERS</span></span>

### <span data-ttu-id="46c1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c1a-111">-DefaultProfile</span></span>
<span data-ttu-id="46c1a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46c1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46c1a-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="46c1a-113">-Filter</span></span>
<span data-ttu-id="46c1a-114">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="46c1a-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="46c1a-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="46c1a-115">-InlineCount</span></span>
<span data-ttu-id="46c1a-116">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="46c1a-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="46c1a-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="46c1a-117">-OrderBy</span></span>
<span data-ttu-id="46c1a-118">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="46c1a-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="46c1a-119">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="46c1a-119">-Skip</span></span>
<span data-ttu-id="46c1a-120">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="46c1a-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="46c1a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46c1a-121">-SubscriptionId</span></span>
<span data-ttu-id="46c1a-122">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="46c1a-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46c1a-123">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="46c1a-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="46c1a-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="46c1a-124">-Top</span></span>
<span data-ttu-id="46c1a-125">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="46c1a-125">OData top parameter.</span></span>

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

### <span data-ttu-id="46c1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c1a-126">CommonParameters</span></span>
<span data-ttu-id="46c1a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c1a-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46c1a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c1a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46c1a-129">INPUTS</span></span>

## <span data-ttu-id="46c1a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46c1a-130">OUTPUTS</span></span>

### <span data-ttu-id="46c1a-131">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="46c1a-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="46c1a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46c1a-132">NOTES</span></span>

## <span data-ttu-id="46c1a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46c1a-133">RELATED LINKS</span></span>

