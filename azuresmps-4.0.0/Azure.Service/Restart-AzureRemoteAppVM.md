---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099314"
---
# <span data-ttu-id="41634-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="41634-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="41634-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41634-102">SYNOPSIS</span></span>
<span data-ttu-id="41634-103">Startar om en virtuell dator i en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="41634-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="41634-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41634-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41634-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41634-105">DESCRIPTION</span></span>
<span data-ttu-id="41634-106">Cmdleten **restart-AzureRemoteAppVM** startar om en virtuell dator i en Azure RemoteApp-samling där den angivna användaren är ansluten.</span><span class="sxs-lookup"><span data-stu-id="41634-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="41634-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41634-107">EXAMPLES</span></span>

### <span data-ttu-id="41634-108">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="41634-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="41634-109">Det här kommandot startar om en virtuell dator i en Azure RemoteApp-samling med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="41634-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="41634-110">Användaren PattiFuller@contoso.com är ansluten till samlingen som innehåller den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="41634-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="41634-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41634-111">PARAMETERS</span></span>

### <span data-ttu-id="41634-112">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="41634-112">-CollectionName</span></span>
<span data-ttu-id="41634-113">Anger namnet på en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="41634-113">Specifies the name of an Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="41634-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="41634-114">-LogoffMessage</span></span>
<span data-ttu-id="41634-115">Anger ett varnings meddelande som visas för användare som är anslutna till den virtuella datorn innan denna cmdlet loggar ut.</span><span class="sxs-lookup"><span data-stu-id="41634-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41634-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="41634-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="41634-117">Anger hur länge denna cmdlet ska vänta innan den loggar användare av.</span><span class="sxs-lookup"><span data-stu-id="41634-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="41634-118">Standardvärdet är 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="41634-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41634-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="41634-119">-Profile</span></span>
<span data-ttu-id="41634-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="41634-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41634-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="41634-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41634-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="41634-122">-UserUpn</span></span>
<span data-ttu-id="41634-123">Anger användarens huvud namn (UPN) för den användare vars cmdlet startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="41634-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="41634-124">Använd cmdleten **Get-AzureRemoteAppVM** för att få virtuella datorer i samlingen och anslutna UPN: er.</span><span class="sxs-lookup"><span data-stu-id="41634-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41634-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41634-125">-Confirm</span></span>
<span data-ttu-id="41634-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41634-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41634-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41634-127">-WhatIf</span></span>
<span data-ttu-id="41634-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41634-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41634-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41634-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41634-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41634-130">CommonParameters</span></span>
<span data-ttu-id="41634-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41634-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41634-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41634-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41634-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41634-133">INPUTS</span></span>

## <span data-ttu-id="41634-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41634-134">OUTPUTS</span></span>

## <span data-ttu-id="41634-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41634-135">NOTES</span></span>

## <span data-ttu-id="41634-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41634-136">RELATED LINKS</span></span>

[<span data-ttu-id="41634-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="41634-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


