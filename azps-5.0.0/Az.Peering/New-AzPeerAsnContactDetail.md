---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269599"
---
# <span data-ttu-id="4510d-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="4510d-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="4510d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4510d-102">SYNOPSIS</span></span>
<span data-ttu-id="4510d-103">Skapar en i minnes kontakt detalj för PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="4510d-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="4510d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4510d-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4510d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4510d-105">DESCRIPTION</span></span>
<span data-ttu-id="4510d-106">Skapa en i minnet PeerAsn kontakt detalj.</span><span class="sxs-lookup"><span data-stu-id="4510d-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="4510d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4510d-107">EXAMPLES</span></span>

### <span data-ttu-id="4510d-108">Skapa kontakt information och lägga till i PeerAsn</span><span class="sxs-lookup"><span data-stu-id="4510d-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="4510d-109">Roll och e-postadress krävs.</span><span class="sxs-lookup"><span data-stu-id="4510d-109">Role and email are required.</span></span> <span data-ttu-id="4510d-110">Telefonen är valfri.</span><span class="sxs-lookup"><span data-stu-id="4510d-110">Phone is optional.</span></span> <span data-ttu-id="4510d-111">Telefon stöder +-() eller blank steg.</span><span class="sxs-lookup"><span data-stu-id="4510d-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="4510d-112">En PeerAsn måste innehålla minst en kontakt information av typen "NOC"</span><span class="sxs-lookup"><span data-stu-id="4510d-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="4510d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4510d-113">PARAMETERS</span></span>

### <span data-ttu-id="4510d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4510d-114">-DefaultProfile</span></span>
<span data-ttu-id="4510d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4510d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4510d-116">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="4510d-116">-Email</span></span>
<span data-ttu-id="4510d-117">E-postadresser som används för att kontakta dig om problem arrise vanligt vis ett nätverks åtgärds Center</span><span class="sxs-lookup"><span data-stu-id="4510d-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="4510d-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="4510d-118">-Phone</span></span>
<span data-ttu-id="4510d-119">Telefon som används för att kontakta om problem arrise vanligt vis ett nätverks åtgärds Center</span><span class="sxs-lookup"><span data-stu-id="4510d-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="4510d-120">-Roll</span><span class="sxs-lookup"><span data-stu-id="4510d-120">-Role</span></span>
<span data-ttu-id="4510d-121">Välj den roll som passar kontakt informationen bäst.</span><span class="sxs-lookup"><span data-stu-id="4510d-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="4510d-122">NOC-kontakt krävs.</span><span class="sxs-lookup"><span data-stu-id="4510d-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="4510d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4510d-123">CommonParameters</span></span>
<span data-ttu-id="4510d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4510d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4510d-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4510d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4510d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4510d-126">INPUTS</span></span>

### <span data-ttu-id="4510d-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="4510d-127">None</span></span>

## <span data-ttu-id="4510d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4510d-128">OUTPUTS</span></span>

### <span data-ttu-id="4510d-129">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="4510d-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="4510d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4510d-130">NOTES</span></span>

## <span data-ttu-id="4510d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4510d-131">RELATED LINKS</span></span>
