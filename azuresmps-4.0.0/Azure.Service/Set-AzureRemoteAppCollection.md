---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099283"
---
# <span data-ttu-id="744a2-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="744a2-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="744a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="744a2-102">SYNOPSIS</span></span>
<span data-ttu-id="744a2-103">Anger egenskaperna för en RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="744a2-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="744a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="744a2-104">SYNTAX</span></span>

### <span data-ttu-id="744a2-105">DescriptionOnly (standard)</span><span class="sxs-lookup"><span data-stu-id="744a2-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="744a2-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="744a2-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="744a2-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="744a2-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="744a2-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="744a2-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="744a2-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="744a2-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="744a2-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="744a2-110">DESCRIPTION</span></span>
<span data-ttu-id="744a2-111">Cmdleten **set-AzureRemoteAppCollection** anger egenskaperna för en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="744a2-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="744a2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="744a2-112">EXAMPLES</span></span>

## <span data-ttu-id="744a2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="744a2-113">PARAMETERS</span></span>

### <span data-ttu-id="744a2-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="744a2-114">-AclLevel</span></span>
<span data-ttu-id="744a2-115">Anger ACL-nivån (Access Control List) för samlingen.</span><span class="sxs-lookup"><span data-stu-id="744a2-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="744a2-116">De acceptabla värdena för den här parametern är: Collection och Application.</span><span class="sxs-lookup"><span data-stu-id="744a2-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-117">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="744a2-117">-CollectionName</span></span>
<span data-ttu-id="744a2-118">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="744a2-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="744a2-119">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="744a2-119">-Credential</span></span>
<span data-ttu-id="744a2-120">Anger autentiseringsuppgifterna för ett tjänst konto som har behörighet att ansluta till din domän Azure RemoteApp-servrar.</span><span class="sxs-lookup"><span data-stu-id="744a2-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="744a2-121">Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="744a2-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="744a2-122">-CustomRdpProperty</span></span>
<span data-ttu-id="744a2-123">Anger anpassade RDP-egenskaper (Remote Desktop Protocol) som kan användas för att konfigurera enhetsomdirigering och andra inställningar.</span><span class="sxs-lookup"><span data-stu-id="744a2-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="744a2-124">Mer information finns i [RDP-inställningar för fjärr skrivbords tjänster i Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="744a2-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="744a2-125">-Description</span></span>
<span data-ttu-id="744a2-126">Anger en kort beskrivning för samlingen.</span><span class="sxs-lookup"><span data-stu-id="744a2-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-127">-Planera</span><span class="sxs-lookup"><span data-stu-id="744a2-127">-Plan</span></span>
<span data-ttu-id="744a2-128">Anger abonnemanget för Azure RemoteApp-samlingen, som definierar användnings gränserna.</span><span class="sxs-lookup"><span data-stu-id="744a2-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="744a2-129">Använd **Get-AzureRemoteAppPlan** för att se vilka abonnemang som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="744a2-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a2-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="744a2-130">-Profile</span></span>
<span data-ttu-id="744a2-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="744a2-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="744a2-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="744a2-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="744a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744a2-133">CommonParameters</span></span>
<span data-ttu-id="744a2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744a2-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744a2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744a2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="744a2-136">INPUTS</span></span>

## <span data-ttu-id="744a2-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="744a2-137">OUTPUTS</span></span>

## <span data-ttu-id="744a2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="744a2-138">NOTES</span></span>

## <span data-ttu-id="744a2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="744a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="744a2-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="744a2-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="744a2-141">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="744a2-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="744a2-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="744a2-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


