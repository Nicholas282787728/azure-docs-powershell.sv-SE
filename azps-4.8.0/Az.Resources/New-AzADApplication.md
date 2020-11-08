---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258701"
---
# <span data-ttu-id="8d15c-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8d15c-101">New-AzADApplication</span></span>

## <span data-ttu-id="8d15c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d15c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d15c-103">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="8d15c-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="8d15c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d15c-104">SYNTAX</span></span>

### <span data-ttu-id="8d15c-105">ApplicationWithoutCredentialParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8d15c-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d15c-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d15c-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d15c-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d15c-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d15c-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d15c-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d15c-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d15c-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d15c-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d15c-110">DESCRIPTION</span></span>
<span data-ttu-id="8d15c-111">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="8d15c-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="8d15c-112">Nedan följer de behörigheter som krävs för att skapa ett program:</span><span class="sxs-lookup"><span data-stu-id="8d15c-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="8d15c-113">Azure Active Directory-diagram</span><span class="sxs-lookup"><span data-stu-id="8d15c-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="8d15c-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="8d15c-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="8d15c-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8d15c-115">Microsoft Graph</span></span>
  - <span data-ttu-id="8d15c-116">Katalog. AccessAsUser. all</span><span class="sxs-lookup"><span data-stu-id="8d15c-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="8d15c-117">Directory. ReadWrite. all</span><span class="sxs-lookup"><span data-stu-id="8d15c-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="8d15c-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d15c-118">EXAMPLES</span></span>

### <span data-ttu-id="8d15c-119">Exempel 1: skapa ett nytt AAD-program.</span><span class="sxs-lookup"><span data-stu-id="8d15c-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="8d15c-120">Skapar ett nytt Azure Active Directory-program utan några autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="8d15c-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="8d15c-121">Exempel 2: skapa nytt AAD-program med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="8d15c-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="8d15c-122">Skapar ett nytt Azure Active Directory-program och kopplar lösen ord till dem.</span><span class="sxs-lookup"><span data-stu-id="8d15c-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="8d15c-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d15c-123">PARAMETERS</span></span>

### <span data-ttu-id="8d15c-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="8d15c-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="8d15c-125">Det värde som anger om programmet är en enskild klient organisation eller en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="8d15c-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="8d15c-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="8d15c-126">-CertValue</span></span>
<span data-ttu-id="8d15c-127">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="8d15c-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="8d15c-128">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="8d15c-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="8d15c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d15c-129">-DefaultProfile</span></span>
<span data-ttu-id="8d15c-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8d15c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d15c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8d15c-131">-DisplayName</span></span>
<span data-ttu-id="8d15c-132">Visnings namn för det nya programmet.</span><span class="sxs-lookup"><span data-stu-id="8d15c-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="8d15c-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8d15c-133">-EndDate</span></span>
<span data-ttu-id="8d15c-134">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="8d15c-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="8d15c-135">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="8d15c-135">The default end date value is one year from today.</span></span> <span data-ttu-id="8d15c-136">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="8d15c-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="8d15c-137">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="8d15c-137">-HomePage</span></span>
<span data-ttu-id="8d15c-138">URL-adressen till program start sidan.</span><span class="sxs-lookup"><span data-stu-id="8d15c-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="8d15c-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="8d15c-139">-IdentifierUris</span></span>
<span data-ttu-id="8d15c-140">URI: erna som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="8d15c-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="8d15c-141">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="8d15c-141">-KeyCredentials</span></span>
<span data-ttu-id="8d15c-142">Listan med autentiseringsuppgifter som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="8d15c-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d15c-143">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="8d15c-143">-Password</span></span>
<span data-ttu-id="8d15c-144">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="8d15c-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="8d15c-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="8d15c-145">-PasswordCredentials</span></span>
<span data-ttu-id="8d15c-146">Listan med autentiseringsuppgifter för lösen ord som är kopplade till programmet.</span><span class="sxs-lookup"><span data-stu-id="8d15c-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d15c-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="8d15c-147">-ReplyUrls</span></span>
<span data-ttu-id="8d15c-148">URL: en för programsvaret.</span><span class="sxs-lookup"><span data-stu-id="8d15c-148">The application reply urls.</span></span>

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

### <span data-ttu-id="8d15c-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="8d15c-149">-StartDate</span></span>
<span data-ttu-id="8d15c-150">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="8d15c-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="8d15c-151">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="8d15c-151">The default start date value is today.</span></span> <span data-ttu-id="8d15c-152">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="8d15c-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="8d15c-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d15c-153">-Confirm</span></span>
<span data-ttu-id="8d15c-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d15c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d15c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d15c-155">-WhatIf</span></span>
<span data-ttu-id="8d15c-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d15c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d15c-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d15c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d15c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d15c-158">CommonParameters</span></span>
<span data-ttu-id="8d15c-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d15c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d15c-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d15c-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d15c-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d15c-161">INPUTS</span></span>

### <span data-ttu-id="8d15c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="8d15c-162">System.String</span></span>

### <span data-ttu-id="8d15c-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="8d15c-163">System.String[]</span></span>

### <span data-ttu-id="8d15c-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d15c-164">System.Boolean</span></span>

### <span data-ttu-id="8d15c-165">Microsoft. Azure. commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="8d15c-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="8d15c-166">Microsoft. Azure. commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="8d15c-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="8d15c-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="8d15c-167">System.Security.SecureString</span></span>

### <span data-ttu-id="8d15c-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8d15c-168">System.DateTime</span></span>

## <span data-ttu-id="8d15c-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d15c-169">OUTPUTS</span></span>

### <span data-ttu-id="8d15c-170">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8d15c-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8d15c-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d15c-171">NOTES</span></span>
<span data-ttu-id="8d15c-172">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="8d15c-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8d15c-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d15c-173">RELATED LINKS</span></span>

[<span data-ttu-id="8d15c-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8d15c-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="8d15c-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8d15c-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="8d15c-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8d15c-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="8d15c-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8d15c-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="8d15c-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8d15c-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8d15c-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8d15c-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

