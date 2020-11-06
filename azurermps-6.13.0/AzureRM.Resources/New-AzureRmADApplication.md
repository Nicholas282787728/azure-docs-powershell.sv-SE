---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: e23e3db6cb574fb16b2c559c948372c808840de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576779"
---
# <span data-ttu-id="50656-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50656-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="50656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50656-102">SYNOPSIS</span></span>
<span data-ttu-id="50656-103">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="50656-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50656-104">SYNTAX</span></span>

### <span data-ttu-id="50656-105">ApplicationWithoutCredentialParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="50656-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50656-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50656-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50656-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50656-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50656-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50656-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50656-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50656-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50656-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50656-110">DESCRIPTION</span></span>
<span data-ttu-id="50656-111">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="50656-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="50656-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50656-112">EXAMPLES</span></span>

### <span data-ttu-id="50656-113">Exempel 1 – Skapa nytt AAD-program.</span><span class="sxs-lookup"><span data-stu-id="50656-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="50656-114">Skapar ett nytt Azure Active Directory-program utan några autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="50656-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="50656-115">Exempel 2 – Skapa ett nytt AAD-program med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="50656-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="50656-116">Skapar ett nytt Azure Active Directory-program och kopplar lösen ord till dem.</span><span class="sxs-lookup"><span data-stu-id="50656-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="50656-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50656-117">PARAMETERS</span></span>

### <span data-ttu-id="50656-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="50656-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="50656-119">Det värde som anger om programmet är en enskild klient organisation eller en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="50656-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="50656-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="50656-120">-CertValue</span></span>
<span data-ttu-id="50656-121">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="50656-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="50656-122">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="50656-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="50656-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50656-123">-DefaultProfile</span></span>
<span data-ttu-id="50656-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="50656-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50656-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50656-125">-DisplayName</span></span>
<span data-ttu-id="50656-126">Visnings namn för det nya programmet.</span><span class="sxs-lookup"><span data-stu-id="50656-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="50656-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="50656-127">-EndDate</span></span>
<span data-ttu-id="50656-128">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="50656-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="50656-129">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="50656-129">The default end date value is one year from today.</span></span> <span data-ttu-id="50656-130">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="50656-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="50656-131">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="50656-131">-HomePage</span></span>
<span data-ttu-id="50656-132">URL-adressen till program start sidan.</span><span class="sxs-lookup"><span data-stu-id="50656-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="50656-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="50656-133">-IdentifierUris</span></span>
<span data-ttu-id="50656-134">URI: erna som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="50656-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="50656-135">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="50656-135">-KeyCredentials</span></span>
<span data-ttu-id="50656-136">Listan med autentiseringsuppgifter som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="50656-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="50656-137">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="50656-137">-Password</span></span>
<span data-ttu-id="50656-138">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="50656-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="50656-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="50656-139">-PasswordCredentials</span></span>
<span data-ttu-id="50656-140">Listan med autentiseringsuppgifter för lösen ord som är kopplade till programmet.</span><span class="sxs-lookup"><span data-stu-id="50656-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="50656-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="50656-141">-ReplyUrls</span></span>
<span data-ttu-id="50656-142">URL: en för programsvaret.</span><span class="sxs-lookup"><span data-stu-id="50656-142">The application reply urls.</span></span>

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

### <span data-ttu-id="50656-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="50656-143">-StartDate</span></span>
<span data-ttu-id="50656-144">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="50656-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="50656-145">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="50656-145">The default start date value is today.</span></span> <span data-ttu-id="50656-146">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="50656-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="50656-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50656-147">-Confirm</span></span>
<span data-ttu-id="50656-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50656-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50656-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50656-149">-WhatIf</span></span>
<span data-ttu-id="50656-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50656-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50656-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50656-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50656-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50656-152">CommonParameters</span></span>
<span data-ttu-id="50656-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50656-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50656-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50656-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50656-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50656-155">INPUTS</span></span>

### <span data-ttu-id="50656-156">System. String</span><span class="sxs-lookup"><span data-stu-id="50656-156">System.String</span></span>

### <span data-ttu-id="50656-157">System. string []</span><span class="sxs-lookup"><span data-stu-id="50656-157">System.String[]</span></span>

### <span data-ttu-id="50656-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50656-158">System.Boolean</span></span>

### <span data-ttu-id="50656-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="50656-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="50656-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="50656-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="50656-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="50656-161">System.Security.SecureString</span></span>

### <span data-ttu-id="50656-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="50656-162">System.DateTime</span></span>

## <span data-ttu-id="50656-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50656-163">OUTPUTS</span></span>

### <span data-ttu-id="50656-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="50656-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="50656-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50656-165">NOTES</span></span>
<span data-ttu-id="50656-166">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="50656-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="50656-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50656-167">RELATED LINKS</span></span>

[<span data-ttu-id="50656-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50656-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="50656-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50656-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="50656-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50656-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="50656-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50656-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="50656-172">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50656-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="50656-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50656-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

