---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099625"
---
# <span data-ttu-id="b82b4-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b82b4-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="b82b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b82b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b82b4-103">Överför ett certifikat till en Azure Cloud-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b82b4-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="b82b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b82b4-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b82b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b82b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b82b4-106">Cmdleten **Add-AzureCertificate** laddar upp ett certifikat för en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b82b4-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="b82b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b82b4-107">EXAMPLES</span></span>

### <span data-ttu-id="b82b4-108">Exempel 1: Ladda upp ett certifikat och lösen ord</span><span class="sxs-lookup"><span data-stu-id="b82b4-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="b82b4-109">Det här kommandot laddar upp certifikat filen ContosoCertificate. pfx till en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="b82b4-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="b82b4-110">Kommandot anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b82b4-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="b82b4-111">Exempel 2: Ladda upp en certifikat fil</span><span class="sxs-lookup"><span data-stu-id="b82b4-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="b82b4-112">Det här kommandot laddar upp certifikat filen ContosoCertificate. cer till en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="b82b4-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="b82b4-113">Kommandot anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b82b4-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="b82b4-114">Exempel 3: Ladda upp ett certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="b82b4-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="b82b4-115">Det första kommandot får ett certifikat från min butik av en användare med hjälp av cmdleten för Windows PowerShell Core **Get-item** .</span><span class="sxs-lookup"><span data-stu-id="b82b4-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="b82b4-116">Kommandot lagrar certifikatet i $Certificate variabel.</span><span class="sxs-lookup"><span data-stu-id="b82b4-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="b82b4-117">Det andra kommandot laddar upp certifikatet i $certificate till en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="b82b4-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="b82b4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b82b4-118">PARAMETERS</span></span>

### <span data-ttu-id="b82b4-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="b82b4-119">-CertToDeploy</span></span>
<span data-ttu-id="b82b4-120">Anger vilket certifikat som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="b82b4-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="b82b4-121">Du kan ange den fullständiga sökvägen till en certifikat fil, till exempel en fil som har \*. cer eller \*.</span><span class="sxs-lookup"><span data-stu-id="b82b4-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="b82b4-122">PFX-fil, eller ett certifikat objekt för X. 509.</span><span class="sxs-lookup"><span data-stu-id="b82b4-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b82b4-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b82b4-123">-InformationAction</span></span>
<span data-ttu-id="b82b4-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b82b4-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b82b4-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b82b4-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b82b4-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="b82b4-126">Continue</span></span>
- <span data-ttu-id="b82b4-127">Över</span><span class="sxs-lookup"><span data-stu-id="b82b4-127">Ignore</span></span>
- <span data-ttu-id="b82b4-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="b82b4-128">Inquire</span></span>
- <span data-ttu-id="b82b4-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b82b4-129">SilentlyContinue</span></span>
- <span data-ttu-id="b82b4-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="b82b4-130">Stop</span></span>
- <span data-ttu-id="b82b4-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b82b4-131">Suspend</span></span>

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

### <span data-ttu-id="b82b4-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b82b4-132">-InformationVariable</span></span>
<span data-ttu-id="b82b4-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b82b4-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b82b4-134">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="b82b4-134">-Password</span></span>
<span data-ttu-id="b82b4-135">Anger certifikatets lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b82b4-135">Specifies the certificate password.</span></span>

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

### <span data-ttu-id="b82b4-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="b82b4-136">-Profile</span></span>
<span data-ttu-id="b82b4-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b82b4-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b82b4-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b82b4-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b82b4-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b82b4-139">-ServiceName</span></span>
<span data-ttu-id="b82b4-140">Anger namnet på den Azure-tjänst dit denna cmdlet lägger till ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="b82b4-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82b4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82b4-141">CommonParameters</span></span>
<span data-ttu-id="b82b4-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b82b4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82b4-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b82b4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82b4-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b82b4-144">INPUTS</span></span>

## <span data-ttu-id="b82b4-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b82b4-145">OUTPUTS</span></span>

### <span data-ttu-id="b82b4-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b82b4-146">ManagementOperationContext</span></span>

## <span data-ttu-id="b82b4-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b82b4-147">NOTES</span></span>

## <span data-ttu-id="b82b4-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b82b4-148">RELATED LINKS</span></span>

[<span data-ttu-id="b82b4-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b82b4-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="b82b4-150">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="b82b4-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="b82b4-151">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b82b4-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


