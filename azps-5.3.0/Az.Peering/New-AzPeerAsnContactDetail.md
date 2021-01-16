---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424955"
---
# <span data-ttu-id="9f18c-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="9f18c-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="9f18c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f18c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f18c-103">Skapar en i minnes kontakt detalj för PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="9f18c-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="9f18c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f18c-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f18c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f18c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f18c-106">Skapa en i minnet PeerAsn kontakt detalj.</span><span class="sxs-lookup"><span data-stu-id="9f18c-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="9f18c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f18c-107">EXAMPLES</span></span>

### <span data-ttu-id="9f18c-108">Skapa kontakt information och lägga till i PeerAsn</span><span class="sxs-lookup"><span data-stu-id="9f18c-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="9f18c-109">Roll och e-postadress krävs.</span><span class="sxs-lookup"><span data-stu-id="9f18c-109">Role and email are required.</span></span> <span data-ttu-id="9f18c-110">Telefonen är valfri.</span><span class="sxs-lookup"><span data-stu-id="9f18c-110">Phone is optional.</span></span> <span data-ttu-id="9f18c-111">Telefon stöder +-() eller blank steg.</span><span class="sxs-lookup"><span data-stu-id="9f18c-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="9f18c-112">En PeerAsn måste innehålla minst en kontakt information av typen "NOC"</span><span class="sxs-lookup"><span data-stu-id="9f18c-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="9f18c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f18c-113">PARAMETERS</span></span>

### <span data-ttu-id="9f18c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f18c-114">-DefaultProfile</span></span>
<span data-ttu-id="9f18c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f18c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f18c-116">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="9f18c-116">-Email</span></span>
<span data-ttu-id="9f18c-117">E-postadresser som används för att kontakta dig om problem arrise vanligt vis ett nätverks åtgärds Center</span><span class="sxs-lookup"><span data-stu-id="9f18c-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f18c-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="9f18c-118">-Phone</span></span>
<span data-ttu-id="9f18c-119">Telefon som används för att kontakta om problem arrise vanligt vis ett nätverks åtgärds Center</span><span class="sxs-lookup"><span data-stu-id="9f18c-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="9f18c-120">-Roll</span><span class="sxs-lookup"><span data-stu-id="9f18c-120">-Role</span></span>
<span data-ttu-id="9f18c-121">Välj den roll som passar kontakt informationen bäst.</span><span class="sxs-lookup"><span data-stu-id="9f18c-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="9f18c-122">NOC-kontakt krävs.</span><span class="sxs-lookup"><span data-stu-id="9f18c-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f18c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f18c-123">CommonParameters</span></span>
<span data-ttu-id="9f18c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f18c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f18c-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f18c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f18c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f18c-126">INPUTS</span></span>

### <span data-ttu-id="9f18c-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f18c-127">None</span></span>

## <span data-ttu-id="9f18c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f18c-128">OUTPUTS</span></span>

### <span data-ttu-id="9f18c-129">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="9f18c-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="9f18c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f18c-130">NOTES</span></span>

## <span data-ttu-id="9f18c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f18c-131">RELATED LINKS</span></span>
