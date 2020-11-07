---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756458"
---
# <span data-ttu-id="83965-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="83965-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="83965-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83965-102">SYNOPSIS</span></span>
<span data-ttu-id="83965-103">Lägger till en autentiseringsuppgift i ett befintligt program.</span><span class="sxs-lookup"><span data-stu-id="83965-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83965-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83965-104">SYNTAX</span></span>

### <span data-ttu-id="83965-105">ApplicationObjectIdWithPasswordParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="83965-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83965-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="83965-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83965-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="83965-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83965-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="83965-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83965-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83965-109">DESCRIPTION</span></span>
<span data-ttu-id="83965-110">Med cmdleten New-AzureRmADAppCredential kan du lägga till en ny autentiseringsuppgift eller ställa in autentiseringsuppgifter för ett program.</span><span class="sxs-lookup"><span data-stu-id="83965-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="83965-111">Programmet identifieras genom att ange antingen programobjekt-ID eller program-ID.</span><span class="sxs-lookup"><span data-stu-id="83965-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="83965-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83965-112">EXAMPLES</span></span>

### <span data-ttu-id="83965-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83965-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="83965-114">En ny lösen ords identifiering läggs till i ett befintligt program.</span><span class="sxs-lookup"><span data-stu-id="83965-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="83965-115">I det här exemplet läggs det angivna lösen ordet till i programmet med hjälp av programobjekt-ID.</span><span class="sxs-lookup"><span data-stu-id="83965-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="83965-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="83965-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="83965-117">En ny nyckelinformation läggs till i ett befintligt program.</span><span class="sxs-lookup"><span data-stu-id="83965-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="83965-118">I det här exemplet läggs det tillhandahållna base64-kodade Public X509-certifikatet ("MyApp. cer") till i programmet med hjälp av applicationId.</span><span class="sxs-lookup"><span data-stu-id="83965-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="83965-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="83965-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="83965-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83965-120">PARAMETERS</span></span>

### <span data-ttu-id="83965-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="83965-121">-ApplicationId</span></span>
<span data-ttu-id="83965-122">ID för programmet som du vill lägga till autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="83965-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83965-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="83965-123">-CertValue</span></span>
<span data-ttu-id="83965-124">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="83965-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="83965-125">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="83965-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83965-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83965-126">-DefaultProfile</span></span>
<span data-ttu-id="83965-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="83965-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83965-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="83965-128">-EndDate</span></span>
<span data-ttu-id="83965-129">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="83965-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="83965-130">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="83965-130">The default end date value is one year from today.</span></span> <span data-ttu-id="83965-131">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="83965-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="83965-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="83965-132">-ObjectId</span></span>
<span data-ttu-id="83965-133">Objekt-ID för programmet som du vill lägga till autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="83965-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83965-134">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="83965-134">-Password</span></span>
<span data-ttu-id="83965-135">Lösen ordet som ska kopplas till programmet.</span><span class="sxs-lookup"><span data-stu-id="83965-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83965-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="83965-136">-StartDate</span></span>
<span data-ttu-id="83965-137">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="83965-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="83965-138">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="83965-138">The default start date value is today.</span></span>
<span data-ttu-id="83965-139">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="83965-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="83965-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83965-140">-Confirm</span></span>
<span data-ttu-id="83965-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83965-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83965-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83965-142">-WhatIf</span></span>
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

### <span data-ttu-id="83965-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83965-143">CommonParameters</span></span>
<span data-ttu-id="83965-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83965-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83965-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83965-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83965-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83965-146">INPUTS</span></span>

### <span data-ttu-id="83965-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="83965-147">None</span></span>
<span data-ttu-id="83965-148">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="83965-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83965-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83965-149">OUTPUTS</span></span>

### <span data-ttu-id="83965-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="83965-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="83965-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83965-151">NOTES</span></span>

## <span data-ttu-id="83965-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83965-152">RELATED LINKS</span></span>

[<span data-ttu-id="83965-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="83965-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="83965-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="83965-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="83965-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="83965-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

