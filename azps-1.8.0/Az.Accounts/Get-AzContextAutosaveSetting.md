---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: a6361fabaa05d99b35874ce0de388ed0fc1bdfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743527"
---
# <span data-ttu-id="123ea-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="123ea-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="123ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="123ea-102">SYNOPSIS</span></span>
<span data-ttu-id="123ea-103">Visa metadata om funktionen för Autospara med kontext, inklusive om kontexten sparas automatiskt och om Sparad kontext och autentiseringsinformation kan hittas.</span><span class="sxs-lookup"><span data-stu-id="123ea-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="123ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="123ea-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="123ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="123ea-105">DESCRIPTION</span></span>
<span data-ttu-id="123ea-106">Visa metadata om funktionen för Autospara med kontext, inklusive om kontexten sparas automatiskt och om Sparad kontext och autentiseringsinformation kan hittas.</span><span class="sxs-lookup"><span data-stu-id="123ea-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="123ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="123ea-107">EXAMPLES</span></span>

### <span data-ttu-id="123ea-108">Hämta metadata för den aktuella sessionen</span><span class="sxs-lookup"><span data-stu-id="123ea-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="123ea-109">Få information om huruvida kontexten sparas och om WEHERE.</span><span class="sxs-lookup"><span data-stu-id="123ea-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="123ea-110">I exemplet ovan har funktionen Spara automatiskt avaktiverats.</span><span class="sxs-lookup"><span data-stu-id="123ea-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="123ea-111">Hämta metadata för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="123ea-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="123ea-112">Få information om huruvida kontexten sparas som standard för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="123ea-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="123ea-113">Observera att det här kan skilja sig från inställningarna som är aktiva i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="123ea-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="123ea-114">I exemplet ovan är funktionen Spara automatiskt aktive rad och data sparas på standard platsen.</span><span class="sxs-lookup"><span data-stu-id="123ea-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="123ea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="123ea-115">PARAMETERS</span></span>

### <span data-ttu-id="123ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123ea-116">-DefaultProfile</span></span>
<span data-ttu-id="123ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="123ea-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="123ea-118">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="123ea-118">-Scope</span></span>
<span data-ttu-id="123ea-119">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="123ea-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="123ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123ea-120">CommonParameters</span></span>
<span data-ttu-id="123ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123ea-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="123ea-123">INPUTS</span></span>

### <span data-ttu-id="123ea-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="123ea-124">None</span></span>

## <span data-ttu-id="123ea-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="123ea-125">OUTPUTS</span></span>

### <span data-ttu-id="123ea-126">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="123ea-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="123ea-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="123ea-127">NOTES</span></span>

## <span data-ttu-id="123ea-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="123ea-128">RELATED LINKS</span></span>
