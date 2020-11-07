---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924465"
---
# <span data-ttu-id="0937a-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="0937a-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="0937a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0937a-102">SYNOPSIS</span></span>
<span data-ttu-id="0937a-103">Skapar ett objekt med information om organisation för certifikat i minnet.</span><span class="sxs-lookup"><span data-stu-id="0937a-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="0937a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0937a-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0937a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0937a-105">DESCRIPTION</span></span>
<span data-ttu-id="0937a-106">**New-AzKeyVaultCertificateOrganizationDetails-** cmdleten skapar ett objekt av data organisations information i minnet.</span><span class="sxs-lookup"><span data-stu-id="0937a-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="0937a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0937a-107">EXAMPLES</span></span>

### <span data-ttu-id="0937a-108">Exempel 1: skapa ett objekt med organisationsinformation</span><span class="sxs-lookup"><span data-stu-id="0937a-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="0937a-109">Det första kommandot skapar ett informations objekt för certifikat administratören och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="0937a-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="0937a-110">Det andra kommandot skapar ett objekt för information om certifikat organisation och lagrar det sedan i $OrgDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="0937a-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="0937a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0937a-111">PARAMETERS</span></span>

### <span data-ttu-id="0937a-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="0937a-112">-AdministratorDetails</span></span>
<span data-ttu-id="0937a-113">Anger administratören för certifikat organisation.</span><span class="sxs-lookup"><span data-stu-id="0937a-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0937a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0937a-114">-DefaultProfile</span></span>
<span data-ttu-id="0937a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0937a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0937a-116">-ID</span><span class="sxs-lookup"><span data-stu-id="0937a-116">-Id</span></span>
<span data-ttu-id="0937a-117">Anger organisationens identifierare.</span><span class="sxs-lookup"><span data-stu-id="0937a-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0937a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0937a-118">-Confirm</span></span>
<span data-ttu-id="0937a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0937a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0937a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0937a-120">-WhatIf</span></span>
<span data-ttu-id="0937a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0937a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0937a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0937a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0937a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0937a-123">CommonParameters</span></span>
<span data-ttu-id="0937a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0937a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0937a-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0937a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0937a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0937a-126">INPUTS</span></span>

### <span data-ttu-id="0937a-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="0937a-127">None</span></span>
<span data-ttu-id="0937a-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0937a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0937a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0937a-129">OUTPUTS</span></span>

### <span data-ttu-id="0937a-130">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="0937a-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="0937a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0937a-131">NOTES</span></span>

## <span data-ttu-id="0937a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0937a-132">RELATED LINKS</span></span>

[<span data-ttu-id="0937a-133">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="0937a-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

