---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 98f127386a606881a0f8359e605ee2b96168a9b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927254"
---
# <span data-ttu-id="19cc9-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="19cc9-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="19cc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="19cc9-103">Lägger till en autentiseringsuppgift till ett befintligt tjänst huvud konto.</span><span class="sxs-lookup"><span data-stu-id="19cc9-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="19cc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19cc9-104">SYNTAX</span></span>

### <span data-ttu-id="19cc9-105">SpObjectIdWithPasswordParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="19cc9-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cc9-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="19cc9-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cc9-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="19cc9-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cc9-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="19cc9-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cc9-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="19cc9-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cc9-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="19cc9-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19cc9-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19cc9-111">DESCRIPTION</span></span>
<span data-ttu-id="19cc9-112">New-AzADSpCredential cmdleten kan användas för att lägga till en ny autentiseringsuppgift eller för att lyfta autentiseringsuppgifter för ett tjänst huvud konto.</span><span class="sxs-lookup"><span data-stu-id="19cc9-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="19cc9-113">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID: t eller SPN.</span><span class="sxs-lookup"><span data-stu-id="19cc9-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="19cc9-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19cc9-114">EXAMPLES</span></span>

### <span data-ttu-id="19cc9-115">Exempel 1 – Skapa en ny tjänst säkerhets referens med ett genererat lösen ord</span><span class="sxs-lookup"><span data-stu-id="19cc9-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="19cc9-116">En ny lösen ords identifiering läggs till i det befintliga tjänst säkerhets objekt med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="19cc9-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="19cc9-117">Exempel 2 – Skapa en ny tjänst säkerhets referens med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="19cc9-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="19cc9-118">Det tillhandahållna base64-kodade X509-certifikatet ("MyApp. cer") läggs till i det befintliga tjänst säkerhets objekt med dess SPN.</span><span class="sxs-lookup"><span data-stu-id="19cc9-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="19cc9-119">Exempel 3 – skapa en ny tjänst huvud referenser med ledning</span><span class="sxs-lookup"><span data-stu-id="19cc9-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="19cc9-120">Hämtar tjänstens huvud namn med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' och rör till New-AzADSpCredential för att skapa en ny tjänst huvud identifiering för den tjänstens huvud konto med ett genererat lösen ord.</span><span class="sxs-lookup"><span data-stu-id="19cc9-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="19cc9-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19cc9-121">PARAMETERS</span></span>

### <span data-ttu-id="19cc9-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="19cc9-122">-CertValue</span></span>
<span data-ttu-id="19cc9-123">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="19cc9-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="19cc9-124">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="19cc9-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="19cc9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cc9-125">-DefaultProfile</span></span>
<span data-ttu-id="19cc9-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="19cc9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cc9-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="19cc9-127">-EndDate</span></span>
<span data-ttu-id="19cc9-128">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="19cc9-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="19cc9-129">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="19cc9-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="19cc9-130">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="19cc9-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="19cc9-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="19cc9-131">-ObjectId</span></span>
<span data-ttu-id="19cc9-132">Objekt-ID för tjänstens huvud namn att lägga till autentiseringsuppgifterna i.</span><span class="sxs-lookup"><span data-stu-id="19cc9-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19cc9-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="19cc9-133">-ServicePrincipalName</span></span>
<span data-ttu-id="19cc9-134">Namnet (SPN) för tjänstens huvud namn för att lägga till autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="19cc9-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="19cc9-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="19cc9-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="19cc9-136">Tjänst huvud objekt för att lägga till autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="19cc9-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19cc9-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="19cc9-137">-StartDate</span></span>
<span data-ttu-id="19cc9-138">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="19cc9-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="19cc9-139">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="19cc9-139">The default start date value is today.</span></span>
<span data-ttu-id="19cc9-140">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="19cc9-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="19cc9-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19cc9-141">-Confirm</span></span>
<span data-ttu-id="19cc9-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19cc9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cc9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cc9-143">-WhatIf</span></span>
<span data-ttu-id="19cc9-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19cc9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19cc9-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19cc9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cc9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cc9-146">CommonParameters</span></span>
<span data-ttu-id="19cc9-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19cc9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cc9-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19cc9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cc9-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19cc9-149">INPUTS</span></span>

### <span data-ttu-id="19cc9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="19cc9-150">System.String</span></span>

### <span data-ttu-id="19cc9-151">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="19cc9-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="19cc9-152">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="19cc9-152">System.DateTime</span></span>

## <span data-ttu-id="19cc9-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19cc9-153">OUTPUTS</span></span>

### <span data-ttu-id="19cc9-154">Microsoft. Azure. commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="19cc9-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="19cc9-155">Microsoft. Azure. kommandon. sources. Models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="19cc9-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="19cc9-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19cc9-156">NOTES</span></span>

## <span data-ttu-id="19cc9-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19cc9-157">RELATED LINKS</span></span>

[<span data-ttu-id="19cc9-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="19cc9-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="19cc9-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="19cc9-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="19cc9-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="19cc9-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



