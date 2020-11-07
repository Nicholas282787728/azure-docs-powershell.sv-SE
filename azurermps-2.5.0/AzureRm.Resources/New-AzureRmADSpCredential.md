---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 2f4a5e19f9b563361b526fab386c068fe65ce6ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930865"
---
# <span data-ttu-id="07ef0-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07ef0-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="07ef0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="07ef0-103">Lägger till en autentiseringsuppgift till ett befintligt tjänst huvud konto.</span><span class="sxs-lookup"><span data-stu-id="07ef0-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07ef0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07ef0-104">SYNTAX</span></span>

### <span data-ttu-id="07ef0-105">SpObjectIdWithPasswordParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="07ef0-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07ef0-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="07ef0-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07ef0-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="07ef0-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07ef0-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="07ef0-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07ef0-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="07ef0-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07ef0-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="07ef0-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07ef0-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07ef0-111">DESCRIPTION</span></span>
<span data-ttu-id="07ef0-112">New-AzureRmADSpCredential cmdleten kan användas för att lägga till en ny autentiseringsuppgift eller för att lyfta autentiseringsuppgifter för ett tjänst huvud konto.</span><span class="sxs-lookup"><span data-stu-id="07ef0-112">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="07ef0-113">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID: t eller SPN.</span><span class="sxs-lookup"><span data-stu-id="07ef0-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="07ef0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07ef0-114">EXAMPLES</span></span>

### <span data-ttu-id="07ef0-115">Exempel 1 – Skapa en ny tjänst säkerhets referens med ett genererat lösen ord</span><span class="sxs-lookup"><span data-stu-id="07ef0-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="07ef0-116">En ny lösen ords identifiering läggs till i det befintliga tjänst säkerhets objekt med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="07ef0-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="07ef0-117">Exempel 2 – Skapa en ny tjänst säkerhets referens med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="07ef0-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="07ef0-118">Det tillhandahållna base64-kodade X509-certifikatet ("MyApp. cer") läggs till i det befintliga tjänst säkerhets objekt med dess SPN.</span><span class="sxs-lookup"><span data-stu-id="07ef0-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="07ef0-119">Exempel 3 – skapa en ny tjänst huvud referenser med ledning</span><span class="sxs-lookup"><span data-stu-id="07ef0-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzureRmADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="07ef0-120">Hämtar tjänstens huvud namn med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' och rör till New-AzureRmADSpCredential för att skapa en ny tjänst huvud identifiering för den tjänstens huvud konto med ett genererat lösen ord.</span><span class="sxs-lookup"><span data-stu-id="07ef0-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzureRmADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="07ef0-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07ef0-121">PARAMETERS</span></span>

### <span data-ttu-id="07ef0-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="07ef0-122">-CertValue</span></span>
<span data-ttu-id="07ef0-123">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="07ef0-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="07ef0-124">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="07ef0-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ef0-125">-DefaultProfile</span></span>
<span data-ttu-id="07ef0-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="07ef0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="07ef0-127">-EndDate</span></span>
<span data-ttu-id="07ef0-128">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="07ef0-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="07ef0-129">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="07ef0-129">The default end date value is one year from today.</span></span> <span data-ttu-id="07ef0-130">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="07ef0-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="07ef0-131">-ObjectId</span></span>
<span data-ttu-id="07ef0-132">Objekt-ID för tjänstens huvud namn att lägga till autentiseringsuppgifterna i.</span><span class="sxs-lookup"><span data-stu-id="07ef0-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-133">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="07ef0-133">-Password</span></span>
<span data-ttu-id="07ef0-134">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="07ef0-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="07ef0-135">-ServicePrincipalName</span></span>
<span data-ttu-id="07ef0-136">Namnet (SPN) för tjänstens huvud namn för att lägga till autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="07ef0-136">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="07ef0-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="07ef0-138">Tjänst huvud objekt för att lägga till autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="07ef0-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="07ef0-139">-StartDate</span></span>
<span data-ttu-id="07ef0-140">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="07ef0-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="07ef0-141">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="07ef0-141">The default start date value is today.</span></span> <span data-ttu-id="07ef0-142">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="07ef0-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07ef0-143">-Confirm</span></span>
<span data-ttu-id="07ef0-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07ef0-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ef0-145">-WhatIf</span></span>
<span data-ttu-id="07ef0-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07ef0-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ef0-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07ef0-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ef0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ef0-148">CommonParameters</span></span>
<span data-ttu-id="07ef0-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ef0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ef0-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ef0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ef0-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07ef0-151">INPUTS</span></span>

### <span data-ttu-id="07ef0-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="07ef0-152">System.Guid</span></span>

### <span data-ttu-id="07ef0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="07ef0-153">System.String</span></span>

### <span data-ttu-id="07ef0-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07ef0-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="07ef0-155">Parametrar: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="07ef0-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="07ef0-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="07ef0-156">System.Security.SecureString</span></span>

### <span data-ttu-id="07ef0-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="07ef0-157">System.DateTime</span></span>

## <span data-ttu-id="07ef0-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07ef0-158">OUTPUTS</span></span>

### <span data-ttu-id="07ef0-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="07ef0-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="07ef0-160">Microsoft. Azure. kommandon. sources. Models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="07ef0-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="07ef0-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07ef0-161">NOTES</span></span>

## <span data-ttu-id="07ef0-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07ef0-162">RELATED LINKS</span></span>

[<span data-ttu-id="07ef0-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07ef0-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="07ef0-164">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07ef0-164">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="07ef0-165">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07ef0-165">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



