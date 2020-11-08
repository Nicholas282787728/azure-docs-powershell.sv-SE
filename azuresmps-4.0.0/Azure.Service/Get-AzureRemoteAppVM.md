---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099801"
---
# <span data-ttu-id="29280-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="29280-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="29280-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29280-102">SYNOPSIS</span></span>
<span data-ttu-id="29280-103">Hämtar de virtuella datorerna i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="29280-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="29280-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29280-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29280-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29280-105">DESCRIPTION</span></span>
<span data-ttu-id="29280-106">Cmdleten **Get-AzureRemoteAppVM** hämtar de virtuella datorerna som skapades under en Azure RemoteApp-samling för värdskap.</span><span class="sxs-lookup"><span data-stu-id="29280-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="29280-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29280-107">EXAMPLES</span></span>

### <span data-ttu-id="29280-108">Exempel 1: Visa de virtuella datorerna i en samling</span><span class="sxs-lookup"><span data-stu-id="29280-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="29280-109">Det här kommandot visar de virtuella datorer som används för att logga in i en Azure RemoteApp-samling med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="29280-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="29280-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29280-110">PARAMETERS</span></span>

### <span data-ttu-id="29280-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="29280-111">-CollectionName</span></span>
<span data-ttu-id="29280-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="29280-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="29280-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="29280-113">-Profile</span></span>
<span data-ttu-id="29280-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="29280-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29280-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="29280-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29280-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29280-116">CommonParameters</span></span>
<span data-ttu-id="29280-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29280-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29280-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29280-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29280-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29280-119">INPUTS</span></span>

## <span data-ttu-id="29280-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29280-120">OUTPUTS</span></span>

## <span data-ttu-id="29280-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29280-121">NOTES</span></span>

## <span data-ttu-id="29280-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29280-122">RELATED LINKS</span></span>

[<span data-ttu-id="29280-123">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="29280-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


