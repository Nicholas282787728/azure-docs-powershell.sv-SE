---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522605"
---
# <span data-ttu-id="2661d-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="2661d-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="2661d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2661d-102">SYNOPSIS</span></span>
<span data-ttu-id="2661d-103">Skapar ett objekt med information om organisation för certifikat i minnet.</span><span class="sxs-lookup"><span data-stu-id="2661d-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="2661d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2661d-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2661d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2661d-105">DESCRIPTION</span></span>
<span data-ttu-id="2661d-106">**New-AzKeyVaultCertificateOrganizationDetail-** cmdleten skapar ett objekt av data organisations information i minnet.</span><span class="sxs-lookup"><span data-stu-id="2661d-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="2661d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2661d-107">EXAMPLES</span></span>

### <span data-ttu-id="2661d-108">Exempel 1: skapa ett objekt med organisationsinformation</span><span class="sxs-lookup"><span data-stu-id="2661d-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="2661d-109">Det första kommandot skapar ett informations objekt för certifikat administratören och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="2661d-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="2661d-110">Det andra kommandot skapar ett objekt för information om certifikat organisation och lagrar det sedan i $OrgDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="2661d-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="2661d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2661d-111">PARAMETERS</span></span>

### <span data-ttu-id="2661d-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="2661d-112">-AdministratorDetails</span></span>
<span data-ttu-id="2661d-113">Anger administratören för certifikat organisation.</span><span class="sxs-lookup"><span data-stu-id="2661d-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2661d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2661d-114">-DefaultProfile</span></span>
<span data-ttu-id="2661d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2661d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2661d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2661d-116">-Id</span></span>
<span data-ttu-id="2661d-117">Anger organisationens identifierare.</span><span class="sxs-lookup"><span data-stu-id="2661d-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="2661d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2661d-118">-Confirm</span></span>
<span data-ttu-id="2661d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2661d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2661d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2661d-120">-WhatIf</span></span>
<span data-ttu-id="2661d-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2661d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2661d-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2661d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2661d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2661d-123">CommonParameters</span></span>
<span data-ttu-id="2661d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2661d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2661d-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2661d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2661d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2661d-126">INPUTS</span></span>

### <span data-ttu-id="2661d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2661d-127">System.String</span></span>

### <span data-ttu-id="2661d-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. publicKeyToken. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. PowerShell. cmdletar. valv, version = 1.0.0.0, Culture = neutral, = null]]</span><span class="sxs-lookup"><span data-stu-id="2661d-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2661d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2661d-129">OUTPUTS</span></span>

### <span data-ttu-id="2661d-130">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2661d-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="2661d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2661d-131">NOTES</span></span>

## <span data-ttu-id="2661d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2661d-132">RELATED LINKS</span></span>

[<span data-ttu-id="2661d-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="2661d-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

