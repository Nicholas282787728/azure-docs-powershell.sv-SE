---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093429"
---
# <span data-ttu-id="732f6-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="732f6-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="732f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="732f6-102">SYNOPSIS</span></span>
<span data-ttu-id="732f6-103">Tar bort objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="732f6-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="732f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="732f6-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="732f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="732f6-105">DESCRIPTION</span></span>
<span data-ttu-id="732f6-106">Cmdleten **Clear-AzureRemoteAppVmStaleAdObject** tar bort objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.</span><span class="sxs-lookup"><span data-stu-id="732f6-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="732f6-107">Du måste använda autentiseringsuppgifter som har behörighet att ta bort Azure Active Directory-objekt.</span><span class="sxs-lookup"><span data-stu-id="732f6-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="732f6-108">Om du anger parametern *verbose* visas namnet på varje objekt som tas bort.</span><span class="sxs-lookup"><span data-stu-id="732f6-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="732f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="732f6-109">EXAMPLES</span></span>

### <span data-ttu-id="732f6-110">Exempel 1: ta bort inaktuella objekt för en samling</span><span class="sxs-lookup"><span data-stu-id="732f6-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="732f6-111">I det första kommandot uppmanas du att ange ett användar namn och lösen ord med hjälp av **Hämta-Credential**.</span><span class="sxs-lookup"><span data-stu-id="732f6-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="732f6-112">Kommandot lagrar resultaten i variabeln $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="732f6-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="732f6-113">Det andra kommandot rensar de inaktuella objekten för samlingen contoso.</span><span class="sxs-lookup"><span data-stu-id="732f6-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="732f6-114">Kommandot använder autentiseringsuppgifterna som lagras i $AdminCredentials variabel.</span><span class="sxs-lookup"><span data-stu-id="732f6-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="732f6-115">Dessa autentiseringsuppgifter måste ha rätt behörighet för att kommandot ska fungera.</span><span class="sxs-lookup"><span data-stu-id="732f6-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="732f6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="732f6-116">PARAMETERS</span></span>

### <span data-ttu-id="732f6-117">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="732f6-117">-CollectionName</span></span>
<span data-ttu-id="732f6-118">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="732f6-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="732f6-119">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="732f6-119">-Credential</span></span>
<span data-ttu-id="732f6-120">Anger en autentiseringsuppgift som har behörighet att utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="732f6-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="732f6-121">Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="732f6-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="732f6-122">Om du inte anger den här parametern används den aktuella användarens autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="732f6-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="732f6-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="732f6-123">-Profile</span></span>
<span data-ttu-id="732f6-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="732f6-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="732f6-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="732f6-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="732f6-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="732f6-126">-Confirm</span></span>
<span data-ttu-id="732f6-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="732f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732f6-128">-WhatIf</span></span>
<span data-ttu-id="732f6-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="732f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="732f6-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="732f6-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732f6-131">CommonParameters</span></span>
<span data-ttu-id="732f6-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="732f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732f6-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732f6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732f6-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="732f6-134">INPUTS</span></span>

## <span data-ttu-id="732f6-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="732f6-135">OUTPUTS</span></span>

## <span data-ttu-id="732f6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="732f6-136">NOTES</span></span>

## <span data-ttu-id="732f6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="732f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="732f6-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="732f6-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


