---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099162"
---
# <span data-ttu-id="cbb26-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="cbb26-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="cbb26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbb26-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb26-103">Skapar ett objekt för ett certifikat i en tjänst.</span><span class="sxs-lookup"><span data-stu-id="cbb26-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="cbb26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbb26-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cbb26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbb26-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb26-106">Cmdleten **New-AzureCertificateSetting** skapar ett objekt för ett certifikat i en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="cbb26-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="cbb26-107">Du kan använda ett certifikat inställnings objekt för att skapa ett konfigurations objekt med hjälp av cmdleten **Add-AzureProvisioningConfig** .</span><span class="sxs-lookup"><span data-stu-id="cbb26-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="cbb26-108">Använd ett konfigurations objekt för att skapa en virtuell dator med cmdleten **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="cbb26-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="cbb26-109">Du kan använda ett certifikat inställnings objekt för att skapa en virtuell dator med cmdleten **New-AzureQuickVM** .</span><span class="sxs-lookup"><span data-stu-id="cbb26-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="cbb26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbb26-110">EXAMPLES</span></span>

### <span data-ttu-id="cbb26-111">Exempel 1: skapa ett objekt för certifikat inställning</span><span class="sxs-lookup"><span data-stu-id="cbb26-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="cbb26-112">Det här kommandot skapar ett objekt för en inställning för ett befintligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="cbb26-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="cbb26-113">Exempel 2: skapa en virtuell dator som använder ett konfigurations inställnings objekt</span><span class="sxs-lookup"><span data-stu-id="cbb26-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="cbb26-114">Det första kommandot lägger till certifikatet ContosoCert. cer till tjänsten som heter ContosoService genom att använda cmdleten **Add-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="cbb26-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="cbb26-115">Det andra kommandot skapar ett objekt för en inställning för certifikat och lagrar det sedan i $CertificateSetting variabel.</span><span class="sxs-lookup"><span data-stu-id="cbb26-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="cbb26-116">Det tredje kommandot får en bild från bild databasen med cmdleten **Get-AzureVMImage** .</span><span class="sxs-lookup"><span data-stu-id="cbb26-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="cbb26-117">Det här kommandot lagrar bilden i variabeln $Image.</span><span class="sxs-lookup"><span data-stu-id="cbb26-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="cbb26-118">Med kommandot slut skapas ett konfigurations objekt för virtuell dator baserat på bilden i $Image genom att använda cmdleten **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="cbb26-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="cbb26-119">Kommandot skickar det objektet till cmdleten **Add-AzureProvisioningConfig** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="cbb26-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cbb26-120">Denna cmdlet lägger till konfigurations information till konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="cbb26-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="cbb26-121">Kommandot skickar objektet till cmdleten **New-AzureVM** , vilket skapar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cbb26-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="cbb26-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbb26-122">PARAMETERS</span></span>

### <span data-ttu-id="cbb26-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cbb26-123">-InformationAction</span></span>
<span data-ttu-id="cbb26-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="cbb26-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cbb26-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cbb26-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbb26-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="cbb26-126">Continue</span></span>
- <span data-ttu-id="cbb26-127">Över</span><span class="sxs-lookup"><span data-stu-id="cbb26-127">Ignore</span></span>
- <span data-ttu-id="cbb26-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="cbb26-128">Inquire</span></span>
- <span data-ttu-id="cbb26-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cbb26-129">SilentlyContinue</span></span>
- <span data-ttu-id="cbb26-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="cbb26-130">Stop</span></span>
- <span data-ttu-id="cbb26-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="cbb26-131">Suspend</span></span>

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

### <span data-ttu-id="cbb26-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cbb26-132">-InformationVariable</span></span>
<span data-ttu-id="cbb26-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="cbb26-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cbb26-134">-Butiks namn</span><span class="sxs-lookup"><span data-stu-id="cbb26-134">-StoreName</span></span>
<span data-ttu-id="cbb26-135">Anger certifikat arkivet där certifikatet ska placeras.</span><span class="sxs-lookup"><span data-stu-id="cbb26-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="cbb26-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="cbb26-136">Valid values are:</span></span> 

- <span data-ttu-id="cbb26-137">Adress boks</span><span class="sxs-lookup"><span data-stu-id="cbb26-137">AddressBook</span></span>
- <span data-ttu-id="cbb26-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="cbb26-138">AuthRoot</span></span>
- <span data-ttu-id="cbb26-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="cbb26-139">CertificateAuthority</span></span>
- <span data-ttu-id="cbb26-140">Är inte tillåtna</span><span class="sxs-lookup"><span data-stu-id="cbb26-140">Disallowed</span></span>
- <span data-ttu-id="cbb26-141">Kalendern</span><span class="sxs-lookup"><span data-stu-id="cbb26-141">My</span></span>
- <span data-ttu-id="cbb26-142">Enhet</span><span class="sxs-lookup"><span data-stu-id="cbb26-142">Root</span></span>
- <span data-ttu-id="cbb26-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="cbb26-143">TrustedPeople</span></span>
- <span data-ttu-id="cbb26-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="cbb26-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbb26-145">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="cbb26-145">-Thumbprint</span></span>
<span data-ttu-id="cbb26-146">Anger tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="cbb26-146">Specifies the thumbprint of the certificate.</span></span>

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

### <span data-ttu-id="cbb26-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb26-147">CommonParameters</span></span>
<span data-ttu-id="cbb26-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb26-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb26-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbb26-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb26-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbb26-150">INPUTS</span></span>

## <span data-ttu-id="cbb26-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbb26-151">OUTPUTS</span></span>

## <span data-ttu-id="cbb26-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbb26-152">NOTES</span></span>

## <span data-ttu-id="cbb26-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbb26-153">RELATED LINKS</span></span>

[<span data-ttu-id="cbb26-154">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb26-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="cbb26-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="cbb26-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="cbb26-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb26-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="cbb26-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="cbb26-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="cbb26-158">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="cbb26-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="cbb26-159">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbb26-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="cbb26-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb26-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


