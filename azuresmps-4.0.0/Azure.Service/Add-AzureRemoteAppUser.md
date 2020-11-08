---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099611"
---
# <span data-ttu-id="c3ed6-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="c3ed6-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="c3ed6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ed6-103">Lägger till en användare i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c3ed6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3ed6-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3ed6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ed6-106">Cmdleten **Add-AzureRemoteAppUser** lägger till en användare i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c3ed6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ed6-108">Exempel 1: lägga till en användare med ett Microsoft-konto</span><span class="sxs-lookup"><span data-stu-id="c3ed6-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="c3ed6-109">Det här kommandot lägger till Microsoft-kontot PattiFuller@contoso.com till samlingen contoso.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="c3ed6-110">Exempel 2: lägga till en användare med ett Azure Active Directory-konto</span><span class="sxs-lookup"><span data-stu-id="c3ed6-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="c3ed6-111">Det här kommandot lägger till Azure Active Directory-kontot PattiFuller@contoso.com till samlingen contoso.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="c3ed6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3ed6-112">PARAMETERS</span></span>

### <span data-ttu-id="c3ed6-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="c3ed6-113">-Alias</span></span>
<span data-ttu-id="c3ed6-114">Anger ett publicerat programalias.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-114">Specifies a published program alias.</span></span>
<span data-ttu-id="c3ed6-115">Du kan bara använda den här parametern i publicerings läget per app.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-115">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="c3ed6-116">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="c3ed6-116">-CollectionName</span></span>
<span data-ttu-id="c3ed6-117">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="c3ed6-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="c3ed6-118">-Profile</span></span>
<span data-ttu-id="c3ed6-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3ed6-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3ed6-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="c3ed6-121">-Type</span></span>
<span data-ttu-id="c3ed6-122">Anger en användar typ.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-122">Specifies a user type.</span></span>
<span data-ttu-id="c3ed6-123">De acceptabla värdena för den här parametern är: OrgId eller MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="c3ed6-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="c3ed6-124">-UserUpn</span></span>
<span data-ttu-id="c3ed6-125">Anger användarens huvud namn (UPN) för en användare, till exempel PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="c3ed6-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="c3ed6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ed6-126">CommonParameters</span></span>
<span data-ttu-id="c3ed6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ed6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ed6-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ed6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ed6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3ed6-129">INPUTS</span></span>

## <span data-ttu-id="c3ed6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3ed6-130">OUTPUTS</span></span>

## <span data-ttu-id="c3ed6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3ed6-131">NOTES</span></span>

## <span data-ttu-id="c3ed6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3ed6-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3ed6-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="c3ed6-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="c3ed6-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="c3ed6-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


