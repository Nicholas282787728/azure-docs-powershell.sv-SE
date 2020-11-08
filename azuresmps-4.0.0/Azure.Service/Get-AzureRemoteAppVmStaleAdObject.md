---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093356"
---
# <span data-ttu-id="f68f3-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="f68f3-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="f68f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f68f3-102">SYNOPSIS</span></span>
<span data-ttu-id="f68f3-103">Hämtar objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="f68f3-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="f68f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f68f3-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f68f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f68f3-105">DESCRIPTION</span></span>
<span data-ttu-id="f68f3-106">Cmdleten **Get-AzureRemoteAppVmStaleAdObject** hämtar objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="f68f3-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="f68f3-107">Denna cmdlet visar namnet på varje objekt som det får.</span><span class="sxs-lookup"><span data-stu-id="f68f3-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="f68f3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f68f3-108">EXAMPLES</span></span>

### <span data-ttu-id="f68f3-109">Exempel 1: Hämta gamla objekt för en samling</span><span class="sxs-lookup"><span data-stu-id="f68f3-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="f68f3-110">Det här andra kommandot får de inaktuella objekten för samlingen contoso.</span><span class="sxs-lookup"><span data-stu-id="f68f3-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="f68f3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f68f3-111">PARAMETERS</span></span>

### <span data-ttu-id="f68f3-112">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="f68f3-112">-CollectionName</span></span>
<span data-ttu-id="f68f3-113">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="f68f3-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f68f3-114">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="f68f3-114">-Credential</span></span>
<span data-ttu-id="f68f3-115">Anger en autentiseringsuppgift som har behörighet att utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f68f3-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="f68f3-116">Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="f68f3-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="f68f3-117">Om du inte anger den här parametern används den aktuella användarens autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="f68f3-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68f3-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="f68f3-118">-Profile</span></span>
<span data-ttu-id="f68f3-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f68f3-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f68f3-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f68f3-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68f3-121">CommonParameters</span></span>
<span data-ttu-id="f68f3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f68f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68f3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f68f3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68f3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f68f3-124">INPUTS</span></span>

## <span data-ttu-id="f68f3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f68f3-125">OUTPUTS</span></span>

### <span data-ttu-id="f68f3-126">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="f68f3-126">String</span></span>

## <span data-ttu-id="f68f3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f68f3-127">NOTES</span></span>

## <span data-ttu-id="f68f3-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f68f3-128">RELATED LINKS</span></span>

[<span data-ttu-id="f68f3-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="f68f3-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


