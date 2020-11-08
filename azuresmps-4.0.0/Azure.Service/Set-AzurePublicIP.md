---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099185"
---
# <span data-ttu-id="efe6c-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="efe6c-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="efe6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efe6c-102">SYNOPSIS</span></span>
<span data-ttu-id="efe6c-103">Lägger till en offentlig IP-adress till en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="efe6c-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="efe6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efe6c-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="efe6c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efe6c-105">DESCRIPTION</span></span>
<span data-ttu-id="efe6c-106">Cmdleten **set-AzurePublicIP** lägger till en offentlig IP-adress till en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="efe6c-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="efe6c-107">Om du kör denna cmdlet för en befintlig virtuell dator uppdaterar du den virtuella datorn för att genomföra ändringarna.</span><span class="sxs-lookup"><span data-stu-id="efe6c-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="efe6c-108">Du kan ange en domän namns etikett för att skapa en motsvarande DNS-post för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="efe6c-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="efe6c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efe6c-109">EXAMPLES</span></span>

### <span data-ttu-id="efe6c-110">Exempel 1: lägga till en offentlig IP för en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="efe6c-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="efe6c-111">Det här kommandot får den virtuella datorn som heter FTPInstance i tjänsten FTPInAzure med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="efe6c-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="efe6c-112">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="efe6c-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="efe6c-113">Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip.</span><span class="sxs-lookup"><span data-stu-id="efe6c-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="efe6c-114">Kommandot skickar den virtuella datorn till cmdleten **Update-AzureVM** som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="efe6c-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="efe6c-115">Exempel 2: lägga till en offentlig IP-adress på en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="efe6c-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="efe6c-116">Det här kommandot skapar ett konfigurations objekt för virtuell dator med hjälp av cmdleten **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="efe6c-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="efe6c-117">Kommandot skickar det objektet till cmdleten **Add-AzureProvisioningConfig** , som ger ytterligare konfiguration.</span><span class="sxs-lookup"><span data-stu-id="efe6c-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="efe6c-118">Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip.</span><span class="sxs-lookup"><span data-stu-id="efe6c-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="efe6c-119">Kommandot överför konfigurationen till cmdleten **New-AzureVM** , som skapar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="efe6c-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="efe6c-120">Exempel 3: lägga till en offentlig IP och etikett till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="efe6c-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="efe6c-121">Det här kommandot får den virtuella datorn som heter FTPInstance i tjänsten FTPInAzure med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="efe6c-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="efe6c-122">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="efe6c-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="efe6c-123">Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip och Label ipname.</span><span class="sxs-lookup"><span data-stu-id="efe6c-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="efe6c-124">Kommandot uppdaterar den virtuella datorn som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="efe6c-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="efe6c-125">Exempel 4: lägga till en offentlig IP och etikett på en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="efe6c-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="efe6c-126">Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar sedan objektet till **Add-AzureProvisioningConfig** , vilket ger ytterligare konfiguration.</span><span class="sxs-lookup"><span data-stu-id="efe6c-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="efe6c-127">Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip och Label ipname.</span><span class="sxs-lookup"><span data-stu-id="efe6c-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="efe6c-128">Kommandot skapar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="efe6c-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="efe6c-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efe6c-129">PARAMETERS</span></span>

### <span data-ttu-id="efe6c-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="efe6c-130">-DomainNameLabel</span></span>
<span data-ttu-id="efe6c-131">Anger det namn som ska användas för en motsvarande DNS-post för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="efe6c-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe6c-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="efe6c-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="efe6c-133">Anger tids gräns för TCP-timeout i minuter.</span><span class="sxs-lookup"><span data-stu-id="efe6c-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe6c-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="efe6c-134">-InformationAction</span></span>
<span data-ttu-id="efe6c-135">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="efe6c-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="efe6c-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="efe6c-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efe6c-137">Vidare</span><span class="sxs-lookup"><span data-stu-id="efe6c-137">Continue</span></span>
- <span data-ttu-id="efe6c-138">Över</span><span class="sxs-lookup"><span data-stu-id="efe6c-138">Ignore</span></span>
- <span data-ttu-id="efe6c-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="efe6c-139">Inquire</span></span>
- <span data-ttu-id="efe6c-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="efe6c-140">SilentlyContinue</span></span>
- <span data-ttu-id="efe6c-141">Stanna</span><span class="sxs-lookup"><span data-stu-id="efe6c-141">Stop</span></span>
- <span data-ttu-id="efe6c-142">Avbryt</span><span class="sxs-lookup"><span data-stu-id="efe6c-142">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe6c-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="efe6c-143">-InformationVariable</span></span>
<span data-ttu-id="efe6c-144">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="efe6c-144">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe6c-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="efe6c-145">-Profile</span></span>
<span data-ttu-id="efe6c-146">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="efe6c-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="efe6c-147">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="efe6c-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="efe6c-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="efe6c-148">-PublicIPName</span></span>
<span data-ttu-id="efe6c-149">Anger det offentliga IP-namnet.</span><span class="sxs-lookup"><span data-stu-id="efe6c-149">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe6c-150">-VM</span><span class="sxs-lookup"><span data-stu-id="efe6c-150">-VM</span></span>
<span data-ttu-id="efe6c-151">Anger den virtuella dator där denna cmdlet lägger till offentlig IP.</span><span class="sxs-lookup"><span data-stu-id="efe6c-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efe6c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe6c-152">CommonParameters</span></span>
<span data-ttu-id="efe6c-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe6c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe6c-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe6c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe6c-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efe6c-155">INPUTS</span></span>

## <span data-ttu-id="efe6c-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efe6c-156">OUTPUTS</span></span>

### <span data-ttu-id="efe6c-157">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="efe6c-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="efe6c-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efe6c-158">NOTES</span></span>

## <span data-ttu-id="efe6c-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efe6c-159">RELATED LINKS</span></span>

[<span data-ttu-id="efe6c-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="efe6c-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="efe6c-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="efe6c-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="efe6c-162">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="efe6c-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="efe6c-163">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="efe6c-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="efe6c-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="efe6c-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="efe6c-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="efe6c-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


