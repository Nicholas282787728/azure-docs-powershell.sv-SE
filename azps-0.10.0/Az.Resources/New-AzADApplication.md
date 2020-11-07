---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 3850e5f142e7ec1496ace1225ab53c160794775a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923961"
---
# <span data-ttu-id="122c8-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="122c8-101">New-AzADApplication</span></span>

## <span data-ttu-id="122c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="122c8-102">SYNOPSIS</span></span>
<span data-ttu-id="122c8-103">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="122c8-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="122c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="122c8-104">SYNTAX</span></span>

### <span data-ttu-id="122c8-105">ApplicationWithoutCredentialParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="122c8-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122c8-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="122c8-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122c8-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="122c8-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122c8-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="122c8-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122c8-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="122c8-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122c8-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="122c8-110">DESCRIPTION</span></span>
<span data-ttu-id="122c8-111">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="122c8-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="122c8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="122c8-112">EXAMPLES</span></span>

### <span data-ttu-id="122c8-113">Exempel 1 – Skapa nytt AAD-program.</span><span class="sxs-lookup"><span data-stu-id="122c8-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="122c8-114">Skapar ett nytt Azure Active Directory-program utan några autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="122c8-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="122c8-115">Exempel 2 – Skapa ett nytt AAD-program med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="122c8-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="122c8-116">Skapar ett nytt Azure Active Directory-program och kopplar lösen ord till dem.</span><span class="sxs-lookup"><span data-stu-id="122c8-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="122c8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="122c8-117">PARAMETERS</span></span>

### <span data-ttu-id="122c8-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="122c8-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="122c8-119">Det värde som anger om programmet är en enskild klient organisation eller en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="122c8-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="122c8-120">-CertValue</span></span>
<span data-ttu-id="122c8-121">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="122c8-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="122c8-122">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="122c8-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122c8-123">-DefaultProfile</span></span>
<span data-ttu-id="122c8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="122c8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="122c8-125">-DisplayName</span></span>
<span data-ttu-id="122c8-126">Visnings namn för det nya programmet.</span><span class="sxs-lookup"><span data-stu-id="122c8-126">Display name of the new application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="122c8-127">-EndDate</span></span>
<span data-ttu-id="122c8-128">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="122c8-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="122c8-129">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="122c8-129">The default end date value is one year from today.</span></span> <span data-ttu-id="122c8-130">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="122c8-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-131">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="122c8-131">-HomePage</span></span>
<span data-ttu-id="122c8-132">URL-adressen till program start sidan.</span><span class="sxs-lookup"><span data-stu-id="122c8-132">The URL to the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="122c8-133">-IdentifierUris</span></span>
<span data-ttu-id="122c8-134">URI: erna som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="122c8-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-135">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="122c8-135">-KeyCredentials</span></span>
<span data-ttu-id="122c8-136">Listan med autentiseringsuppgifter som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="122c8-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-137">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="122c8-137">-Password</span></span>
<span data-ttu-id="122c8-138">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="122c8-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="122c8-139">-PasswordCredentials</span></span>
<span data-ttu-id="122c8-140">Listan med autentiseringsuppgifter för lösen ord som är kopplade till programmet.</span><span class="sxs-lookup"><span data-stu-id="122c8-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="122c8-141">-ReplyUrls</span></span>
<span data-ttu-id="122c8-142">URL: en för programsvaret.</span><span class="sxs-lookup"><span data-stu-id="122c8-142">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="122c8-143">-StartDate</span></span>
<span data-ttu-id="122c8-144">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="122c8-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="122c8-145">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="122c8-145">The default start date value is today.</span></span> <span data-ttu-id="122c8-146">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="122c8-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="122c8-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="122c8-147">-Confirm</span></span>
<span data-ttu-id="122c8-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="122c8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="122c8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122c8-149">-WhatIf</span></span>
<span data-ttu-id="122c8-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="122c8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="122c8-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="122c8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="122c8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122c8-152">CommonParameters</span></span>
<span data-ttu-id="122c8-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122c8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122c8-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122c8-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122c8-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="122c8-155">INPUTS</span></span>

### <span data-ttu-id="122c8-156">System. String</span><span class="sxs-lookup"><span data-stu-id="122c8-156">System.String</span></span>

### <span data-ttu-id="122c8-157">System. string []</span><span class="sxs-lookup"><span data-stu-id="122c8-157">System.String[]</span></span>

### <span data-ttu-id="122c8-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="122c8-158">System.Boolean</span></span>

### <span data-ttu-id="122c8-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="122c8-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="122c8-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="122c8-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="122c8-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="122c8-161">System.Security.SecureString</span></span>

### <span data-ttu-id="122c8-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="122c8-162">System.DateTime</span></span>

## <span data-ttu-id="122c8-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="122c8-163">OUTPUTS</span></span>

### <span data-ttu-id="122c8-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="122c8-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="122c8-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="122c8-165">NOTES</span></span>
<span data-ttu-id="122c8-166">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="122c8-166">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="122c8-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="122c8-167">RELATED LINKS</span></span>

[<span data-ttu-id="122c8-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="122c8-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="122c8-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="122c8-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="122c8-170">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="122c8-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="122c8-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="122c8-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="122c8-172">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="122c8-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="122c8-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="122c8-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

