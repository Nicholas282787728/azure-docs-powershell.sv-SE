---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099549"
---
# <span data-ttu-id="26164-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="26164-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="26164-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26164-102">SYNOPSIS</span></span>
<span data-ttu-id="26164-103">Hämtar egenskaperna för ett eller flera publicerade Azure RemoteApp-program för en samling.</span><span class="sxs-lookup"><span data-stu-id="26164-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="26164-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26164-104">SYNTAX</span></span>

### <span data-ttu-id="26164-105">FilterByName (standard)</span><span class="sxs-lookup"><span data-stu-id="26164-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="26164-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="26164-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="26164-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26164-107">DESCRIPTION</span></span>
<span data-ttu-id="26164-108">Cmdleten **Get-AzureRemoteAppProgram** hämtar egenskaperna för ett eller flera publicerade Azure RemoteApp-program för en samling.</span><span class="sxs-lookup"><span data-stu-id="26164-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="26164-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26164-109">EXAMPLES</span></span>

### <span data-ttu-id="26164-110">Exempel 1: Hämta egenskaper för ett program</span><span class="sxs-lookup"><span data-stu-id="26164-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="26164-111">Det här kommandot visar egenskaperna för ett Azure RemoteApp-program.</span><span class="sxs-lookup"><span data-stu-id="26164-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="26164-112">Programmet "ekonomi program" finns i Azure RemoteApp-samlingen med namnet ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="26164-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="26164-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26164-113">PARAMETERS</span></span>

### <span data-ttu-id="26164-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="26164-114">-Alias</span></span>
<span data-ttu-id="26164-115">Anger alias för det program som du vill hämta egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="26164-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26164-116">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="26164-116">-CollectionName</span></span>
<span data-ttu-id="26164-117">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="26164-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="26164-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="26164-118">-Profile</span></span>
<span data-ttu-id="26164-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="26164-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26164-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="26164-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26164-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="26164-121">-RemoteAppProgram</span></span>
<span data-ttu-id="26164-122">Anger namnet på det program som du vill hämta egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="26164-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="26164-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26164-123">CommonParameters</span></span>
<span data-ttu-id="26164-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26164-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26164-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26164-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26164-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26164-126">INPUTS</span></span>

## <span data-ttu-id="26164-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26164-127">OUTPUTS</span></span>

## <span data-ttu-id="26164-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26164-128">NOTES</span></span>

## <span data-ttu-id="26164-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26164-129">RELATED LINKS</span></span>

[<span data-ttu-id="26164-130">Publicera – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="26164-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="26164-131">Avpublicering – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="26164-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


