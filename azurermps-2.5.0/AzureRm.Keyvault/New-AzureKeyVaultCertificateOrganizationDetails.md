---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930573"
---
# <span data-ttu-id="d7b77-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d7b77-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="d7b77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7b77-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b77-103">Skapar ett objekt med information om organisation för certifikat i minnet.</span><span class="sxs-lookup"><span data-stu-id="d7b77-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7b77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7b77-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7b77-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b77-106">**New-AzureKeyVaultCertificateOrganizationDetails-** cmdleten skapar ett objekt av data organisations information i minnet.</span><span class="sxs-lookup"><span data-stu-id="d7b77-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="d7b77-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7b77-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b77-108">Exempel 1: skapa ett objekt med organisationsinformation</span><span class="sxs-lookup"><span data-stu-id="d7b77-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="d7b77-109">Det första kommandot skapar ett informations objekt för certifikat administratören och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="d7b77-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="d7b77-110">Det andra kommandot skapar ett objekt för information om certifikat organisation och lagrar det sedan i $OrgDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="d7b77-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="d7b77-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7b77-111">PARAMETERS</span></span>

### <span data-ttu-id="d7b77-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d7b77-112">-AdministratorDetails</span></span>
<span data-ttu-id="d7b77-113">Anger administratören för certifikat organisation.</span><span class="sxs-lookup"><span data-stu-id="d7b77-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="d7b77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b77-114">-DefaultProfile</span></span>
<span data-ttu-id="d7b77-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d7b77-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7b77-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d7b77-116">-Id</span></span>
<span data-ttu-id="d7b77-117">Anger organisationens identifierare.</span><span class="sxs-lookup"><span data-stu-id="d7b77-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="d7b77-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7b77-118">-Confirm</span></span>
<span data-ttu-id="d7b77-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7b77-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b77-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b77-120">-WhatIf</span></span>
<span data-ttu-id="d7b77-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7b77-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b77-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7b77-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b77-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b77-123">CommonParameters</span></span>
<span data-ttu-id="d7b77-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b77-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b77-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b77-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b77-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7b77-126">INPUTS</span></span>

## <span data-ttu-id="d7b77-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7b77-127">OUTPUTS</span></span>

### <span data-ttu-id="d7b77-128">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d7b77-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="d7b77-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7b77-129">NOTES</span></span>

## <span data-ttu-id="d7b77-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7b77-130">RELATED LINKS</span></span>

[<span data-ttu-id="d7b77-131">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d7b77-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

