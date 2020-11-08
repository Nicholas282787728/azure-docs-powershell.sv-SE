---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0f1768bec11c5a85e97cdb27e6e9a3195c3880b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916281"
---
# <span data-ttu-id="8deac-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8deac-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8deac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8deac-102">SYNOPSIS</span></span>
<span data-ttu-id="8deac-103">Tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="8deac-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="8deac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8deac-104">SYNTAX</span></span>

### <span data-ttu-id="8deac-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="8deac-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8deac-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8deac-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8deac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8deac-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8deac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8deac-108">DESCRIPTION</span></span>
<span data-ttu-id="8deac-109">Cmdleten **Remove-AzKeyVaultCertificateContact** tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="8deac-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="8deac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8deac-110">EXAMPLES</span></span>

### <span data-ttu-id="8deac-111">Exempel 1: ta bort en certifikat kontakt</span><span class="sxs-lookup"><span data-stu-id="8deac-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="8deac-112">Det här kommandot tar bort Patti Nilsson som en certifikat kontakt för Contoso01-.</span><span class="sxs-lookup"><span data-stu-id="8deac-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="8deac-113">Om PassThru anges returnerar cmdleten listan över återstående certifikat kontakter.</span><span class="sxs-lookup"><span data-stu-id="8deac-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="8deac-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8deac-114">PARAMETERS</span></span>

### <span data-ttu-id="8deac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8deac-115">-DefaultProfile</span></span>
<span data-ttu-id="8deac-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8deac-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8deac-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8deac-117">-EmailAddress</span></span>
<span data-ttu-id="8deac-118">Anger e-postadressen till den kontakt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8deac-118">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8deac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8deac-119">-InputObject</span></span>
<span data-ttu-id="8deac-120">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="8deac-120">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8deac-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8deac-121">-PassThru</span></span>
<span data-ttu-id="8deac-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="8deac-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8deac-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8deac-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8deac-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8deac-124">-ResourceId</span></span>
<span data-ttu-id="8deac-125">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="8deac-125">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8deac-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8deac-126">-VaultName</span></span>
<span data-ttu-id="8deac-127">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="8deac-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8deac-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8deac-128">-Confirm</span></span>
<span data-ttu-id="8deac-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8deac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8deac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8deac-130">-WhatIf</span></span>
<span data-ttu-id="8deac-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8deac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8deac-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8deac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8deac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8deac-133">CommonParameters</span></span>
<span data-ttu-id="8deac-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8deac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8deac-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8deac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8deac-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8deac-136">INPUTS</span></span>

### <span data-ttu-id="8deac-137">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8deac-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8deac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8deac-138">System.String</span></span>

## <span data-ttu-id="8deac-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8deac-139">OUTPUTS</span></span>

### <span data-ttu-id="8deac-140">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8deac-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8deac-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8deac-141">NOTES</span></span>

## <span data-ttu-id="8deac-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8deac-142">RELATED LINKS</span></span>

[<span data-ttu-id="8deac-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8deac-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="8deac-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8deac-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)
