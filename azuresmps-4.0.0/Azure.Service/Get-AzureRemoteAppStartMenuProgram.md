---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099545"
---
# <span data-ttu-id="1e912-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="1e912-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="1e912-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e912-102">SYNOPSIS</span></span>
<span data-ttu-id="1e912-103">Visar program för Start-menyn i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="1e912-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="1e912-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e912-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e912-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e912-105">DESCRIPTION</span></span>
<span data-ttu-id="1e912-106">Cmdleten **Get-AzureRemoteAppStartMenuProgram** listar Start-menyns program i den mallfil som en Azure RemoteApp-samling använder.</span><span class="sxs-lookup"><span data-stu-id="1e912-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="1e912-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e912-107">EXAMPLES</span></span>

### <span data-ttu-id="1e912-108">Exempel 1: lista med Start-menyns program för en samling</span><span class="sxs-lookup"><span data-stu-id="1e912-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="1e912-109">Det här kommandot returnerar listan med program för Start-menyn för samlingen ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="1e912-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="1e912-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e912-110">PARAMETERS</span></span>

### <span data-ttu-id="1e912-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="1e912-111">-CollectionName</span></span>
<span data-ttu-id="1e912-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="1e912-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1e912-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e912-113">-Profile</span></span>
<span data-ttu-id="1e912-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1e912-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e912-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1e912-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e912-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="1e912-116">-ProgramName</span></span>
<span data-ttu-id="1e912-117">Anger namnet på ett program som du vill visa information om.</span><span class="sxs-lookup"><span data-stu-id="1e912-117">Specifies the name of a program for which to list information.</span></span>

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

### <span data-ttu-id="1e912-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e912-118">CommonParameters</span></span>
<span data-ttu-id="1e912-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e912-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e912-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e912-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e912-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e912-121">INPUTS</span></span>

## <span data-ttu-id="1e912-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e912-122">OUTPUTS</span></span>

## <span data-ttu-id="1e912-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e912-123">NOTES</span></span>

## <span data-ttu-id="1e912-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e912-124">RELATED LINKS</span></span>

[<span data-ttu-id="1e912-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1e912-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


