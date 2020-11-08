---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099226"
---
# <span data-ttu-id="c5bc0-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c5bc0-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="c5bc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bc0-103">Skapar en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c5bc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5bc0-104">SYNTAX</span></span>

### <span data-ttu-id="c5bc0-105">AllParameterSets (standard)</span><span class="sxs-lookup"><span data-stu-id="c5bc0-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c5bc0-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="c5bc0-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5bc0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="c5bc0-108">Cmdleten **New-AzureRemoteAppCollection** skapar en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c5bc0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5bc0-109">EXAMPLES</span></span>

### <span data-ttu-id="c5bc0-110">Exempel 1: skapa en samling</span><span class="sxs-lookup"><span data-stu-id="c5bc0-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="c5bc0-111">Det här kommandot skapar en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="c5bc0-112">Exempel 2: skapa en samling med hjälp av autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="c5bc0-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="c5bc0-113">Det här kommandot skapar en Azure RemoteApp-samling med hjälp av en autentiseringsuppgift från cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="c5bc0-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="c5bc0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5bc0-114">PARAMETERS</span></span>

### <span data-ttu-id="c5bc0-115">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="c5bc0-115">-CollectionName</span></span>
<span data-ttu-id="c5bc0-116">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-116">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="c5bc0-117">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="c5bc0-117">-Credential</span></span>
<span data-ttu-id="c5bc0-118">Anger autentiseringsuppgifterna för ett tjänst konto som har behörighet att ansluta till din domän Azure RemoteApp-servrar.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="c5bc0-119">Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="c5bc0-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="c5bc0-120">-CustomRdpProperty</span></span>
<span data-ttu-id="c5bc0-121">Anger anpassade egenskaper för protocal (RDP) som kan användas för att konfigurera enhetsomdirigering och andra inställningar.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="c5bc0-122">Mer information finns i [RDP-inställningar för fjärr skrivbords tjänster i Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="c5bc0-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c5bc0-123">-Description</span></span>
<span data-ttu-id="c5bc0-124">Anger en kort beskrivning för objektet.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-124">Specifies a short description for the object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="c5bc0-125">-DnsServers</span></span>
<span data-ttu-id="c5bc0-126">Anger en kommaavgränsad lista med IPv4-adresser för DNS-servrarna.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="c5bc0-127">-Domain</span></span>
<span data-ttu-id="c5bc0-128">Anger namnet på den Active Directory Domain Services-domän som ska anslutas till värd servrarna för FJÄRRSKRIVBORDSSESSIONER.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c5bc0-129">-ImageName</span></span>
<span data-ttu-id="c5bc0-130">Anger namnet på Azure RemoteApp-mallen.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-130">Specifies the name of the Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="c5bc0-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="c5bc0-131">-Location</span></span>
<span data-ttu-id="c5bc0-132">Anger Azure-regionen för samlingen.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="c5bc0-133">-OrganizationalUnit</span></span>
<span data-ttu-id="c5bc0-134">Anger namnet på den organisationsenhet som ska anslutas till värd servrarna för FJÄRRSKRIVBORDSSESSIONER, till exempel OU = MyOu, DC = min Domain, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="c5bc0-135">Attribut som ORGANISATIONSENHET och DOMÄNKONTROLLANT måste vara i versaler.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="c5bc0-136">ORGANISATIONSENHETen kan inte ändras efter att samlingen har skapats.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-137">-Planera</span><span class="sxs-lookup"><span data-stu-id="c5bc0-137">-Plan</span></span>
<span data-ttu-id="c5bc0-138">Anger abonnemanget för Azure RemoteApp-samlingen, som kan ange användnings begränsningar.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="c5bc0-139">Använd **Get-AzureRemoteAppPlan** för att se vilka abonnemang som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

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

### <span data-ttu-id="c5bc0-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5bc0-140">-Profile</span></span>
<span data-ttu-id="c5bc0-141">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5bc0-142">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5bc0-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c5bc0-143">-ResourceType</span></span>
<span data-ttu-id="c5bc0-144">Anger mängdens resurs typ.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="c5bc0-145">De acceptabla värdena för denna parameter är: app eller skriv bord.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c5bc0-146">-SubnetName</span></span>
<span data-ttu-id="c5bc0-147">Anger namnet på under nätet i det virtuella nätverk som ska användas för att skapa Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c5bc0-148">-VNetName</span></span>
<span data-ttu-id="c5bc0-149">Anger namnet på ett virtuellt Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bc0-150">CommonParameters</span></span>
<span data-ttu-id="c5bc0-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bc0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bc0-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bc0-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bc0-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5bc0-153">INPUTS</span></span>

## <span data-ttu-id="c5bc0-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5bc0-154">OUTPUTS</span></span>

## <span data-ttu-id="c5bc0-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5bc0-155">NOTES</span></span>

## <span data-ttu-id="c5bc0-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5bc0-156">RELATED LINKS</span></span>

[<span data-ttu-id="c5bc0-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c5bc0-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="c5bc0-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="c5bc0-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="c5bc0-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c5bc0-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="c5bc0-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c5bc0-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="c5bc0-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c5bc0-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


