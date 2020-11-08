---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099114"
---
# <span data-ttu-id="0732e-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="0732e-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="0732e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0732e-102">SYNOPSIS</span></span>
<span data-ttu-id="0732e-103">Publicerar ett Azure RemoteApp-program.</span><span class="sxs-lookup"><span data-stu-id="0732e-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="0732e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0732e-104">SYNTAX</span></span>

### <span data-ttu-id="0732e-105">App-ID (standard)</span><span class="sxs-lookup"><span data-stu-id="0732e-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0732e-106">App-sökväg</span><span class="sxs-lookup"><span data-stu-id="0732e-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0732e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0732e-107">DESCRIPTION</span></span>
<span data-ttu-id="0732e-108">Cmdleten **Publishing-AzureRemoteAppProgram** publicerar ett Azure RemoteApp-program som gör det tillgängligt för användare av Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="0732e-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="0732e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0732e-109">EXAMPLES</span></span>

### <span data-ttu-id="0732e-110">Exempel 1: publicera ett program i en samling</span><span class="sxs-lookup"><span data-stu-id="0732e-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="0732e-111">Det här kommandot publicerar programmet i ContosoApps-samlingen med den angivna *StartMenuAppId* för att lägga till programmet på Start-menyn.</span><span class="sxs-lookup"><span data-stu-id="0732e-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="0732e-112">Det publicerade programmet har visnings namnet "finansierings program".</span><span class="sxs-lookup"><span data-stu-id="0732e-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="0732e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0732e-113">PARAMETERS</span></span>

### <span data-ttu-id="0732e-114">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="0732e-114">-CollectionName</span></span>
<span data-ttu-id="0732e-115">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="0732e-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="0732e-116">-Kommandorad</span><span class="sxs-lookup"><span data-stu-id="0732e-116">-CommandLine</span></span>
<span data-ttu-id="0732e-117">Anger kommando rads argument för det program som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="0732e-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="0732e-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0732e-118">-DisplayName</span></span>
<span data-ttu-id="0732e-119">Anger det användarvänliga visnings namnet för Azure RemoteApp-programmet.</span><span class="sxs-lookup"><span data-stu-id="0732e-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="0732e-120">Användare ser det här som namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="0732e-120">Users see this as the name of the application.</span></span>

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

### <span data-ttu-id="0732e-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="0732e-121">-FileVirtualPath</span></span>
<span data-ttu-id="0732e-122">Anger sökvägen till programmet i program mal len.</span><span class="sxs-lookup"><span data-stu-id="0732e-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732e-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="0732e-123">-Profile</span></span>
<span data-ttu-id="0732e-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0732e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0732e-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0732e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0732e-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="0732e-126">-StartMenuAppId</span></span>
<span data-ttu-id="0732e-127">Anger ett GUID som denna cmdlet använder för att lägga till programmet på Start-menyn.</span><span class="sxs-lookup"><span data-stu-id="0732e-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0732e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0732e-128">CommonParameters</span></span>
<span data-ttu-id="0732e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0732e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0732e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0732e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0732e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0732e-131">INPUTS</span></span>

## <span data-ttu-id="0732e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0732e-132">OUTPUTS</span></span>

## <span data-ttu-id="0732e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0732e-133">NOTES</span></span>

## <span data-ttu-id="0732e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0732e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0732e-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="0732e-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="0732e-136">Avpublicering – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="0732e-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


