---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093424"
---
# <span data-ttu-id="456e8-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="456e8-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="456e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="456e8-102">SYNOPSIS</span></span>
<span data-ttu-id="456e8-103">Kopierar användar disken för en användare från en Azure RemoteApp till en annan.</span><span class="sxs-lookup"><span data-stu-id="456e8-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="456e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="456e8-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="456e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="456e8-105">DESCRIPTION</span></span>
<span data-ttu-id="456e8-106">Cmdleten **copy-AzureRemoteAppUserDisk** kopierar användarens diskett från en Azure RemoteApp till en annan.</span><span class="sxs-lookup"><span data-stu-id="456e8-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="456e8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="456e8-107">EXAMPLES</span></span>

### <span data-ttu-id="456e8-108">Exempel 1: kopiera en användar diskett</span><span class="sxs-lookup"><span data-stu-id="456e8-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="456e8-109">Det här kommandot kopierar användar disken för en Azure Active Directory-användare som har UPN PattiFuller@contoso.com från samlingen Contoso01 till Contoso02.</span><span class="sxs-lookup"><span data-stu-id="456e8-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="456e8-110">Om en användare PattiFuller@contoso.com redan finns på Contoso02 skriver det här kommandot över den.</span><span class="sxs-lookup"><span data-stu-id="456e8-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="456e8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="456e8-111">PARAMETERS</span></span>

### <span data-ttu-id="456e8-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="456e8-112">-DestinationCollectionName</span></span>
<span data-ttu-id="456e8-113">Anger namnet på mål Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="456e8-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456e8-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="456e8-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="456e8-115">Anger att denna cmdlet skriver över en befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="456e8-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="456e8-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="456e8-116">-Profile</span></span>
<span data-ttu-id="456e8-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="456e8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="456e8-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="456e8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="456e8-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="456e8-119">-SourceCollectionName</span></span>
<span data-ttu-id="456e8-120">Anger namnet på käll-Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="456e8-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456e8-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="456e8-121">-UserUpn</span></span>
<span data-ttu-id="456e8-122">Anger användarens huvud namn (UPN) för den användare som den här cmdleten kopierar disken för.</span><span class="sxs-lookup"><span data-stu-id="456e8-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456e8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456e8-123">CommonParameters</span></span>
<span data-ttu-id="456e8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456e8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456e8-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456e8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456e8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="456e8-126">INPUTS</span></span>

## <span data-ttu-id="456e8-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="456e8-127">OUTPUTS</span></span>

## <span data-ttu-id="456e8-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="456e8-128">NOTES</span></span>

## <span data-ttu-id="456e8-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="456e8-129">RELATED LINKS</span></span>

[<span data-ttu-id="456e8-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="456e8-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


