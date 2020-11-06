---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: d0d6c69bb85fcdf851f0f134bb376252525aec91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581060"
---
# <span data-ttu-id="7df1f-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="7df1f-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="7df1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7df1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7df1f-103">Visa metadata om funktionen för Autospara med kontext, inklusive whterh kontexten är automatiskt Aved, och där Sparad kontext och autentiseringsinformation kan hittas.</span><span class="sxs-lookup"><span data-stu-id="7df1f-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7df1f-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7df1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7df1f-105">DESCRIPTION</span></span>
<span data-ttu-id="7df1f-106">Visa metadata om funktionen för Autospara med kontext, inklusive om kontexten sparas automatiskt och om Sparad kontext och autentiseringsinformation kan hittas.</span><span class="sxs-lookup"><span data-stu-id="7df1f-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="7df1f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7df1f-107">EXAMPLES</span></span>

### <span data-ttu-id="7df1f-108">Hämta metadata för den aktuella sessionen</span><span class="sxs-lookup"><span data-stu-id="7df1f-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="7df1f-109">Få information om huruvida kontexten sparas och om WEHERE.</span><span class="sxs-lookup"><span data-stu-id="7df1f-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="7df1f-110">I exemplet ovan har funktionen Spara automatiskt avaktiverats.</span><span class="sxs-lookup"><span data-stu-id="7df1f-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="7df1f-111">Hämta metadata för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="7df1f-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="7df1f-112">Få information om huruvida kontexten sparas som standard för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="7df1f-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="7df1f-113">Observera att det här kan skilja sig från inställningarna som är aktiva i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="7df1f-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="7df1f-114">I exemplet ovan är funktionen Spara automatiskt aktive rad och data sparas på standard platsen.</span><span class="sxs-lookup"><span data-stu-id="7df1f-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="7df1f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7df1f-115">PARAMETERS</span></span>

### <span data-ttu-id="7df1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df1f-116">-DefaultProfile</span></span>
<span data-ttu-id="7df1f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7df1f-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df1f-118">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="7df1f-118">-Scope</span></span>
<span data-ttu-id="7df1f-119">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="7df1f-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df1f-120">CommonParameters</span></span>
<span data-ttu-id="7df1f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df1f-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df1f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df1f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7df1f-123">INPUTS</span></span>

### <span data-ttu-id="7df1f-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="7df1f-124">None</span></span>

## <span data-ttu-id="7df1f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7df1f-125">OUTPUTS</span></span>

### <span data-ttu-id="7df1f-126">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="7df1f-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="7df1f-127">Information om aktuella inställningar för autosparande, inklusive om Spara automatiskt är aktiverat för den aktuella användaren, samt var kontext och autentiseringsuppgifter sparas.</span><span class="sxs-lookup"><span data-stu-id="7df1f-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="7df1f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7df1f-128">NOTES</span></span>

## <span data-ttu-id="7df1f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7df1f-129">RELATED LINKS</span></span>

