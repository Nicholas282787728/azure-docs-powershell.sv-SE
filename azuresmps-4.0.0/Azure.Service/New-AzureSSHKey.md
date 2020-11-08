---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099212"
---
# <span data-ttu-id="ea584-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="ea584-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="ea584-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea584-102">SYNOPSIS</span></span>
<span data-ttu-id="ea584-103">Skapar ett SSH-nyckelattribut för att infoga ett befintligt certifikat i en ny Linux-baserad Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ea584-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="ea584-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea584-104">SYNTAX</span></span>

### <span data-ttu-id="ea584-105">nyckel par</span><span class="sxs-lookup"><span data-stu-id="ea584-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea584-106">publickey</span><span class="sxs-lookup"><span data-stu-id="ea584-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea584-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea584-107">DESCRIPTION</span></span>
<span data-ttu-id="ea584-108">Cmdleten **New-AzureSSHKey** skapar ett SSH Key-objekt för ett certifikat som redan har lagts till i Azure.</span><span class="sxs-lookup"><span data-stu-id="ea584-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="ea584-109">Det här SSH-nyckelvärdet kan sedan användas av **New-AzureProvisioningConfig** när du skapar konfigurationsobjektet för en ny virtuell dator med **nya-AzureVM** eller när du skapar en ny virtuell dator med **New-AzureQuickVM**.</span><span class="sxs-lookup"><span data-stu-id="ea584-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="ea584-110">När du lägger till en del av ett skript för att skapa en virtuell dator läggs den angivna offentliga nyckel-eller nyckel paret till för den nya virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ea584-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="ea584-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea584-111">EXAMPLES</span></span>

### <span data-ttu-id="ea584-112">Exempel 1: skapa ett objekt för certifikat inställning</span><span class="sxs-lookup"><span data-stu-id="ea584-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="ea584-113">Det här kommandot skapar ett objekt för en inställning för ett befintligt certifikat och lagrar sedan objektet i en variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="ea584-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="ea584-114">Exempel 2: lägga till ett certifikat till en tjänst</span><span class="sxs-lookup"><span data-stu-id="ea584-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="ea584-115">Det här kommandot lägger till ett certifikat till en Azure-tjänst och skapar sedan en ny virtuell Linux-dator som använder certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ea584-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="ea584-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea584-116">PARAMETERS</span></span>

### <span data-ttu-id="ea584-117">-Finger avtryck</span><span class="sxs-lookup"><span data-stu-id="ea584-117">-Fingerprint</span></span>
<span data-ttu-id="ea584-118">Anger finger avtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ea584-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="ea584-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea584-119">-InformationAction</span></span>
<span data-ttu-id="ea584-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ea584-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea584-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ea584-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea584-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="ea584-122">Continue</span></span>
- <span data-ttu-id="ea584-123">Över</span><span class="sxs-lookup"><span data-stu-id="ea584-123">Ignore</span></span>
- <span data-ttu-id="ea584-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="ea584-124">Inquire</span></span>
- <span data-ttu-id="ea584-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea584-125">SilentlyContinue</span></span>
- <span data-ttu-id="ea584-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="ea584-126">Stop</span></span>
- <span data-ttu-id="ea584-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ea584-127">Suspend</span></span>

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

### <span data-ttu-id="ea584-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea584-128">-InformationVariable</span></span>
<span data-ttu-id="ea584-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ea584-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea584-130">-Par</span><span class="sxs-lookup"><span data-stu-id="ea584-130">-KeyPair</span></span>
<span data-ttu-id="ea584-131">Anger att den här cmdleten skapar ett objekt för att infoga en SSH-nyckelpar i den nya virtuella dator konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ea584-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea584-132">-Path</span><span class="sxs-lookup"><span data-stu-id="ea584-132">-Path</span></span>
<span data-ttu-id="ea584-133">Anger sökvägen för lagring av den offentliga SSH-tangenten eller nyckel paret.</span><span class="sxs-lookup"><span data-stu-id="ea584-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea584-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="ea584-134">-PublicKey</span></span>
<span data-ttu-id="ea584-135">Anger att den här cmdleten skapar ett objekt för att lägga till en offentlig nycklar i en ny virtuell dator konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea584-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea584-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea584-136">CommonParameters</span></span>
<span data-ttu-id="ea584-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea584-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea584-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea584-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea584-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea584-139">INPUTS</span></span>

## <span data-ttu-id="ea584-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea584-140">OUTPUTS</span></span>

## <span data-ttu-id="ea584-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea584-141">NOTES</span></span>

## <span data-ttu-id="ea584-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea584-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea584-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="ea584-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="ea584-144">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ea584-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ea584-145">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ea584-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ea584-146">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="ea584-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


