---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579436"
---
# <span data-ttu-id="667b0-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="667b0-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="667b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="667b0-102">SYNOPSIS</span></span>
<span data-ttu-id="667b0-103">Lägger till en autentiseringsuppgift till ett befintligt tjänst huvud konto.</span><span class="sxs-lookup"><span data-stu-id="667b0-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="667b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="667b0-104">SYNTAX</span></span>

### <span data-ttu-id="667b0-105">SpObjectIdWithPasswordParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="667b0-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667b0-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="667b0-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667b0-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="667b0-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667b0-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="667b0-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667b0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="667b0-109">DESCRIPTION</span></span>
<span data-ttu-id="667b0-110">New-AzureRmADSpCredential cmdleten kan användas för att lägga till en ny autentiseringsuppgift eller för att lyfta autentiseringsuppgifter för ett tjänst huvud konto.</span><span class="sxs-lookup"><span data-stu-id="667b0-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="667b0-111">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID: t eller SPN.</span><span class="sxs-lookup"><span data-stu-id="667b0-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="667b0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="667b0-112">EXAMPLES</span></span>

### <span data-ttu-id="667b0-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="667b0-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="667b0-114">En ny lösen ords identifiering läggs till i ett befintligt tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="667b0-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="667b0-115">I det här exemplet läggs det angivna lösen ordet till i tjänstens huvud namn med objectId.</span><span class="sxs-lookup"><span data-stu-id="667b0-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="667b0-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="667b0-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="667b0-117">En ny nyckelinformation läggs till i ett befintligt tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="667b0-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="667b0-118">I det här exemplet läggs det tillhandahållna base64-kodade Public X509-certifikatet ("MyApp. cer") till tjänstens huvud namn via dess SPN.</span><span class="sxs-lookup"><span data-stu-id="667b0-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="667b0-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="667b0-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="667b0-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="667b0-120">PARAMETERS</span></span>

### <span data-ttu-id="667b0-121">-CertValue</span><span class="sxs-lookup"><span data-stu-id="667b0-121">-CertValue</span></span>
<span data-ttu-id="667b0-122">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="667b0-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="667b0-123">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="667b0-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667b0-124">-DefaultProfile</span></span>
<span data-ttu-id="667b0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="667b0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="667b0-126">-EndDate</span></span>
<span data-ttu-id="667b0-127">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="667b0-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="667b0-128">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="667b0-128">The default end date value is one year from today.</span></span> <span data-ttu-id="667b0-129">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="667b0-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="667b0-130">-ObjectId</span></span>
<span data-ttu-id="667b0-131">Objekt-ID för tjänstens huvud namn att lägga till autentiseringsuppgifterna i.</span><span class="sxs-lookup"><span data-stu-id="667b0-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-132">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="667b0-132">-Password</span></span>
<span data-ttu-id="667b0-133">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="667b0-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="667b0-134">-ServicePrincipalName</span></span>
<span data-ttu-id="667b0-135">Namnet (SPN) för tjänstens huvud namn för att lägga till autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="667b0-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="667b0-136">-StartDate</span></span>
<span data-ttu-id="667b0-137">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="667b0-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="667b0-138">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="667b0-138">The default start date value is today.</span></span> <span data-ttu-id="667b0-139">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="667b0-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="667b0-140">-Confirm</span></span>
<span data-ttu-id="667b0-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="667b0-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667b0-142">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667b0-143">CommonParameters</span></span>
<span data-ttu-id="667b0-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667b0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667b0-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667b0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667b0-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="667b0-146">INPUTS</span></span>

### <span data-ttu-id="667b0-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="667b0-147">None</span></span>
<span data-ttu-id="667b0-148">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="667b0-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="667b0-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="667b0-149">OUTPUTS</span></span>

### <span data-ttu-id="667b0-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="667b0-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="667b0-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="667b0-151">NOTES</span></span>

## <span data-ttu-id="667b0-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="667b0-152">RELATED LINKS</span></span>

[<span data-ttu-id="667b0-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="667b0-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="667b0-154">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="667b0-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="667b0-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="667b0-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



