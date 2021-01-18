---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521448"
---
# <span data-ttu-id="ac6b9-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ac6b9-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="ac6b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6b9-103">Lägger till en autentiseringsuppgift i ett befintligt program.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="ac6b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac6b9-104">SYNTAX</span></span>

### <span data-ttu-id="ac6b9-105">ApplicationObjectIdWithPasswordParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ac6b9-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6b9-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6b9-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac6b9-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac6b9-113">DESCRIPTION</span></span>
<span data-ttu-id="ac6b9-114">Med cmdleten New-AzADAppCredential kan du lägga till en ny autentiseringsuppgift eller ställa in autentiseringsuppgifter för ett program.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="ac6b9-115">Programmet identifieras genom att ange antingen programobjekt-ID eller program-ID.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="ac6b9-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac6b9-116">EXAMPLES</span></span>

### <span data-ttu-id="ac6b9-117">Exempel 1 – Skapa en ny programautentisering med ett lösen ord</span><span class="sxs-lookup"><span data-stu-id="ac6b9-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="ac6b9-118">En ny lösen ords identifiering läggs till i det befintliga programmet med objekt-ID ' 1f89cf81-0146-4f4e-BEAE-2007d0668416 '.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="ac6b9-119">Exempel 2 – Skapa en ny programautentisering med ett certifikat</span><span class="sxs-lookup"><span data-stu-id="ac6b9-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="ac6b9-120">Det tillhandahållna base64-kodade X509-certifikatet ("MyApp. cer") läggs till i det befintliga programmet med program-ID ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 '.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="ac6b9-121">Exempel 3 – skapa en ny programautentisering genom att använda ledning</span><span class="sxs-lookup"><span data-stu-id="ac6b9-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="ac6b9-122">Hämtar programmet med objekt-ID ' 1f89cf81-0146-4f4e-BEAE-2007d0668416 ' och rör till New-AzADAppCredential för att skapa en ny programautentisering för det programmet med angivet lösen ord.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="ac6b9-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac6b9-123">PARAMETERS</span></span>

### <span data-ttu-id="ac6b9-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ac6b9-124">-ApplicationId</span></span>
<span data-ttu-id="ac6b9-125">Program-ID för programmet som du vill lägga till autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="ac6b9-126">-ApplicationObject</span></span>
<span data-ttu-id="ac6b9-127">Application-objektet som du vill lägga till autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="ac6b9-128">-CertValue</span></span>
<span data-ttu-id="ac6b9-129">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="ac6b9-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="ac6b9-130">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6b9-131">-DefaultProfile</span></span>
<span data-ttu-id="ac6b9-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ac6b9-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac6b9-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ac6b9-133">-DisplayName</span></span>
<span data-ttu-id="ac6b9-134">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ac6b9-135">-EndDate</span></span>
<span data-ttu-id="ac6b9-136">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="ac6b9-137">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="ac6b9-138">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="ac6b9-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ac6b9-139">-ObjectId</span></span>
<span data-ttu-id="ac6b9-140">Objekt-ID för programmet som du vill lägga till autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-141">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="ac6b9-141">-Password</span></span>
<span data-ttu-id="ac6b9-142">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ac6b9-143">-StartDate</span></span>
<span data-ttu-id="ac6b9-144">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="ac6b9-145">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-145">The default start date value is today.</span></span> <span data-ttu-id="ac6b9-146">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="ac6b9-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac6b9-147">-Confirm</span></span>
<span data-ttu-id="ac6b9-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac6b9-149">-WhatIf</span></span>
<span data-ttu-id="ac6b9-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac6b9-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6b9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6b9-152">CommonParameters</span></span>
<span data-ttu-id="ac6b9-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6b9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6b9-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac6b9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6b9-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac6b9-155">INPUTS</span></span>

### <span data-ttu-id="ac6b9-156">System. String</span><span class="sxs-lookup"><span data-stu-id="ac6b9-156">System.String</span></span>

### <span data-ttu-id="ac6b9-157">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ac6b9-157">System.Guid</span></span>

### <span data-ttu-id="ac6b9-158">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ac6b9-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="ac6b9-159">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ac6b9-159">System.Security.SecureString</span></span>

### <span data-ttu-id="ac6b9-160">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ac6b9-160">System.DateTime</span></span>

## <span data-ttu-id="ac6b9-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac6b9-161">OUTPUTS</span></span>

### <span data-ttu-id="ac6b9-162">Microsoft. Azure. commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ac6b9-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ac6b9-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac6b9-163">NOTES</span></span>

## <span data-ttu-id="ac6b9-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac6b9-164">RELATED LINKS</span></span>

[<span data-ttu-id="ac6b9-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ac6b9-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="ac6b9-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ac6b9-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="ac6b9-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ac6b9-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

