---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: c43bba247268d7ffcdbc2c33d7198415738c5694
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585343"
---
# <span data-ttu-id="b654b-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b654b-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="b654b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b654b-102">SYNOPSIS</span></span>
<span data-ttu-id="b654b-103">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="b654b-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b654b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b654b-104">SYNTAX</span></span>

### <span data-ttu-id="b654b-105">ApplicationWithoutCredentialParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b654b-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b654b-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b654b-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b654b-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b654b-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b654b-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b654b-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b654b-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b654b-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b654b-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b654b-110">DESCRIPTION</span></span>
<span data-ttu-id="b654b-111">Skapar ett nytt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="b654b-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="b654b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b654b-112">EXAMPLES</span></span>

### <span data-ttu-id="b654b-113">--------------------------Skapa nytt AAD-program.</span><span class="sxs-lookup"><span data-stu-id="b654b-113">--------------------------  Create new AAD application.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="b654b-114">Skapar ett nytt Azure Active Directory-program utan några autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="b654b-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="b654b-115">--------------------------Skapa nytt AAD-program med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b654b-115">--------------------------  Create new AAD application with password.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password "password"
```

<span data-ttu-id="b654b-116">Skapar ett nytt Azure Active Directory-program och kopplar lösen ord till dem.</span><span class="sxs-lookup"><span data-stu-id="b654b-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="b654b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b654b-117">PARAMETERS</span></span>

### <span data-ttu-id="b654b-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="b654b-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="b654b-119">Det värde som anger om programmet är en enskild klient organisation eller en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="b654b-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="b654b-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b654b-120">-CertValue</span></span>
<span data-ttu-id="b654b-121">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="b654b-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b654b-122">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b654b-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="b654b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b654b-123">-DisplayName</span></span>
<span data-ttu-id="b654b-124">Visnings namn för det nya programmet.</span><span class="sxs-lookup"><span data-stu-id="b654b-124">Display name of the new application.</span></span>

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

### <span data-ttu-id="b654b-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b654b-125">-EndDate</span></span>
<span data-ttu-id="b654b-126">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="b654b-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b654b-127">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="b654b-127">The default end date value is one year from today.</span></span> <span data-ttu-id="b654b-128">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="b654b-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b654b-129">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="b654b-129">-HomePage</span></span>
<span data-ttu-id="b654b-130">URL-adressen till program start sidan.</span><span class="sxs-lookup"><span data-stu-id="b654b-130">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="b654b-131">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="b654b-131">-IdentifierUris</span></span>
<span data-ttu-id="b654b-132">URI: erna som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="b654b-132">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="b654b-133">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="b654b-133">-KeyCredentials</span></span>
<span data-ttu-id="b654b-134">Listan med autentiseringsuppgifter som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="b654b-134">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="b654b-135">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="b654b-135">-Password</span></span>
<span data-ttu-id="b654b-136">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="b654b-136">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b654b-137">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="b654b-137">-PasswordCredentials</span></span>
<span data-ttu-id="b654b-138">Listan med autentiseringsuppgifter för lösen ord som är kopplade till programmet.</span><span class="sxs-lookup"><span data-stu-id="b654b-138">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="b654b-139">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="b654b-139">-ReplyUrls</span></span>
<span data-ttu-id="b654b-140">URL: en för programsvaret.</span><span class="sxs-lookup"><span data-stu-id="b654b-140">The application reply urls.</span></span>

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

### <span data-ttu-id="b654b-141">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b654b-141">-StartDate</span></span>
<span data-ttu-id="b654b-142">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="b654b-142">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b654b-143">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="b654b-143">The default start date value is today.</span></span> <span data-ttu-id="b654b-144">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="b654b-144">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b654b-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b654b-145">-Confirm</span></span>
<span data-ttu-id="b654b-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b654b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b654b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b654b-147">-WhatIf</span></span>
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

### <span data-ttu-id="b654b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b654b-148">-DefaultProfile</span></span>
<span data-ttu-id="b654b-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b654b-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b654b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b654b-150">CommonParameters</span></span>
<span data-ttu-id="b654b-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b654b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b654b-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b654b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b654b-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b654b-153">INPUTS</span></span>

## <span data-ttu-id="b654b-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b654b-154">OUTPUTS</span></span>

### <span data-ttu-id="b654b-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b654b-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="b654b-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b654b-156">NOTES</span></span>
<span data-ttu-id="b654b-157">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b654b-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b654b-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b654b-158">RELATED LINKS</span></span>

[<span data-ttu-id="b654b-159">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b654b-159">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="b654b-160">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b654b-160">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="b654b-161">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b654b-161">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b654b-162">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b654b-162">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="b654b-163">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b654b-163">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="b654b-164">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b654b-164">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

