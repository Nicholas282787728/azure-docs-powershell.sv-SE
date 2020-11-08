---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093402"
---
# <span data-ttu-id="9abaa-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="9abaa-101">Get-AzureAccount</span></span>

## <span data-ttu-id="9abaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9abaa-102">SYNOPSIS</span></span>
<span data-ttu-id="9abaa-103">Får Azure-konton som är tillgängliga för Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9abaa-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="9abaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9abaa-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9abaa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9abaa-105">DESCRIPTION</span></span>
<span data-ttu-id="9abaa-106">Cmdleten **Get-AzureAccount** hämtar de Azure-konton som är tillgängliga för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9abaa-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="9abaa-107">Använd cmdletarna **Add-AzureAccount** eller **import-PublishSettingsFile** för att göra dina konton tillgängliga för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9abaa-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="9abaa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9abaa-108">EXAMPLES</span></span>

### <span data-ttu-id="9abaa-109">Exempel 1: Hämta alla konton</span><span class="sxs-lookup"><span data-stu-id="9abaa-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="9abaa-110">Med det här kommandot hämtas alla konton som är kopplade till angiven användare.</span><span class="sxs-lookup"><span data-stu-id="9abaa-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="9abaa-111">Exempel 2: Hämta ett konto med namn</span><span class="sxs-lookup"><span data-stu-id="9abaa-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="9abaa-112">Det här kommandot får ContosoAdmin-kontot.</span><span class="sxs-lookup"><span data-stu-id="9abaa-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="9abaa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9abaa-113">PARAMETERS</span></span>

### <span data-ttu-id="9abaa-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9abaa-114">-Name</span></span>
<span data-ttu-id="9abaa-115">Hämtar bara det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="9abaa-115">Gets only the specified account.</span></span>
<span data-ttu-id="9abaa-116">Standardinställningen är alla konton som är tillgängliga för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9abaa-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="9abaa-117">Ange konto namnet.</span><span class="sxs-lookup"><span data-stu-id="9abaa-117">Enter the account name.</span></span>
<span data-ttu-id="9abaa-118">**Name** -värdet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="9abaa-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="9abaa-119">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="9abaa-119">Wildcards are not permitted.</span></span>

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

### <span data-ttu-id="9abaa-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="9abaa-120">-Profile</span></span>
<span data-ttu-id="9abaa-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9abaa-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9abaa-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9abaa-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9abaa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abaa-123">CommonParameters</span></span>
<span data-ttu-id="9abaa-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abaa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abaa-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9abaa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abaa-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9abaa-126">INPUTS</span></span>

### <span data-ttu-id="9abaa-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="9abaa-127">None</span></span>
<span data-ttu-id="9abaa-128">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9abaa-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="9abaa-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9abaa-129">OUTPUTS</span></span>

### <span data-ttu-id="9abaa-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="9abaa-130">None</span></span>
<span data-ttu-id="9abaa-131">Denna cmdlet returnerar inte några utdata.</span><span class="sxs-lookup"><span data-stu-id="9abaa-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="9abaa-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9abaa-132">NOTES</span></span>

## <span data-ttu-id="9abaa-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9abaa-133">RELATED LINKS</span></span>

[<span data-ttu-id="9abaa-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="9abaa-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="9abaa-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9abaa-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="9abaa-136">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9abaa-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="9abaa-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="9abaa-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


