---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099546"
---
# <span data-ttu-id="8d3e4-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8d3e4-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="8d3e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d3e4-103">Visar en lista över användare i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8d3e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d3e4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8d3e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d3e4-105">DESCRIPTION</span></span>
<span data-ttu-id="8d3e4-106">Cmdleten **Get-AzureRemoteAppUser** visar användarna i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8d3e4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d3e4-107">EXAMPLES</span></span>

### <span data-ttu-id="8d3e4-108">Exempel 1: lista användare av en samling</span><span class="sxs-lookup"><span data-stu-id="8d3e4-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="8d3e4-109">Det här kommandot visar de användare som har åtkomst till Azure RemoteApp-samlingen contoso.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="8d3e4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d3e4-110">PARAMETERS</span></span>

### <span data-ttu-id="8d3e4-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="8d3e4-111">-Alias</span></span>
<span data-ttu-id="8d3e4-112">Anger ett publicerat programalias.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-112">Specifies a published program alias.</span></span>
<span data-ttu-id="8d3e4-113">Du kan bara använda den här parametern i publicerings läget per app.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-113">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3e4-114">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="8d3e4-114">-CollectionName</span></span>
<span data-ttu-id="8d3e4-115">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-115">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3e4-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d3e4-116">-Profile</span></span>
<span data-ttu-id="8d3e4-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d3e4-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d3e4-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="8d3e4-119">-UserUpn</span></span>
<span data-ttu-id="8d3e4-120">Anger användarens huvud namn (UPN) för en användare som ska visa information om.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="8d3e4-121">Till exempel PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8d3e4-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8d3e4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3e4-122">CommonParameters</span></span>
<span data-ttu-id="8d3e4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d3e4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3e4-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d3e4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3e4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d3e4-125">INPUTS</span></span>

## <span data-ttu-id="8d3e4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d3e4-126">OUTPUTS</span></span>

## <span data-ttu-id="8d3e4-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d3e4-127">NOTES</span></span>

## <span data-ttu-id="8d3e4-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d3e4-128">RELATED LINKS</span></span>

[<span data-ttu-id="8d3e4-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8d3e4-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="8d3e4-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="8d3e4-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="8d3e4-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8d3e4-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


