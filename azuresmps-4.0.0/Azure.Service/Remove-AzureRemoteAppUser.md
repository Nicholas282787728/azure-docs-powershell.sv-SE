---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099096"
---
# <span data-ttu-id="51b47-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="51b47-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="51b47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51b47-102">SYNOPSIS</span></span>
<span data-ttu-id="51b47-103">Tar bort en användare från en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="51b47-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="51b47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51b47-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51b47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51b47-105">DESCRIPTION</span></span>
<span data-ttu-id="51b47-106">Cmdleten **Remove-AzureRemoteAppUser** tar bort en användare från en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="51b47-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="51b47-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51b47-107">EXAMPLES</span></span>

### <span data-ttu-id="51b47-108">Example1: ta bort en användare från en samling</span><span class="sxs-lookup"><span data-stu-id="51b47-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="51b47-109">Det här kommandot tar bort Azure ActiveDirectory-användaren PattiFuller@contoso.com från samlingen contoso.</span><span class="sxs-lookup"><span data-stu-id="51b47-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="51b47-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51b47-110">PARAMETERS</span></span>

### <span data-ttu-id="51b47-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="51b47-111">-Alias</span></span>
<span data-ttu-id="51b47-112">Anger ett publicerat programalias.</span><span class="sxs-lookup"><span data-stu-id="51b47-112">Specifies a published program alias.</span></span>
<span data-ttu-id="51b47-113">Du kan bara använda den här parametern i publicerings läget per app.</span><span class="sxs-lookup"><span data-stu-id="51b47-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="51b47-114">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="51b47-114">-CollectionName</span></span>
<span data-ttu-id="51b47-115">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="51b47-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="51b47-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="51b47-116">-Profile</span></span>
<span data-ttu-id="51b47-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="51b47-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51b47-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="51b47-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51b47-119">– Skriv</span><span class="sxs-lookup"><span data-stu-id="51b47-119">-Type</span></span>
<span data-ttu-id="51b47-120">Anger en användar typ.</span><span class="sxs-lookup"><span data-stu-id="51b47-120">Specifies a user type.</span></span>
<span data-ttu-id="51b47-121">De acceptabla värdena för den här parametern är: OrgId eller MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="51b47-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b47-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="51b47-122">-UserUpn</span></span>
<span data-ttu-id="51b47-123">Anger användarens huvud namn (UPN) för en användare, till exempel user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="51b47-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b47-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b47-124">CommonParameters</span></span>
<span data-ttu-id="51b47-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b47-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b47-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b47-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b47-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51b47-127">INPUTS</span></span>

## <span data-ttu-id="51b47-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51b47-128">OUTPUTS</span></span>

## <span data-ttu-id="51b47-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51b47-129">NOTES</span></span>

## <span data-ttu-id="51b47-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51b47-130">RELATED LINKS</span></span>

[<span data-ttu-id="51b47-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="51b47-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="51b47-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="51b47-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


