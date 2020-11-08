---
external help file: Azs.KeyVault.Admin-help.xml
Module Name: Azs.Keyvault.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 435db6fd34e36e6c65b9086b7ac1935f60d86c06
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921455"
---
# <span data-ttu-id="819ca-101">Get-AzsKeyVaultQuota</span><span class="sxs-lookup"><span data-stu-id="819ca-101">Get-AzsKeyVaultQuota</span></span>

## <span data-ttu-id="819ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="819ca-102">SYNOPSIS</span></span>
<span data-ttu-id="819ca-103">Få en lista över alla kvot objekt för ett valv på en plats.</span><span class="sxs-lookup"><span data-stu-id="819ca-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="819ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="819ca-104">SYNTAX</span></span>

```
Get-AzsKeyVaultQuota [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="819ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="819ca-105">DESCRIPTION</span></span>
<span data-ttu-id="819ca-106">Få en lista över alla kvot objekt för ett valv på en plats.</span><span class="sxs-lookup"><span data-stu-id="819ca-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="819ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="819ca-107">EXAMPLES</span></span>

### <span data-ttu-id="819ca-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="819ca-108">EXAMPLE 1</span></span>
```
Get-AzsKeyVaultQuota
```

<span data-ttu-id="819ca-109">Få en lista över alla kvot objekt för ett valv på en plats.</span><span class="sxs-lookup"><span data-stu-id="819ca-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="819ca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="819ca-110">PARAMETERS</span></span>

### <span data-ttu-id="819ca-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="819ca-111">-Location</span></span>
<span data-ttu-id="819ca-112">Plats för kvoten.</span><span class="sxs-lookup"><span data-stu-id="819ca-112">The location of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819ca-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819ca-113">CommonParameters</span></span>
<span data-ttu-id="819ca-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819ca-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819ca-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819ca-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819ca-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="819ca-116">INPUTS</span></span>

## <span data-ttu-id="819ca-117">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="819ca-117">OUTPUTS</span></span>

### <span data-ttu-id="819ca-118">Microsoft. AzureStack. Management. valv. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="819ca-118">Microsoft.AzureStack.Management.KeyVault.Admin.Models.Quota</span></span>

## <span data-ttu-id="819ca-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="819ca-119">NOTES</span></span>

## <span data-ttu-id="819ca-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="819ca-120">RELATED LINKS</span></span>