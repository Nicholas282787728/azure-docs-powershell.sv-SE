---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273456"
---
# <span data-ttu-id="43869-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="43869-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="43869-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43869-102">SYNOPSIS</span></span>
<span data-ttu-id="43869-103">Hämtar kontakter som är registrerade för certifikat aviseringar för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="43869-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="43869-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43869-104">SYNTAX</span></span>

### <span data-ttu-id="43869-105">VaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="43869-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43869-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="43869-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43869-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="43869-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43869-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43869-108">DESCRIPTION</span></span>
<span data-ttu-id="43869-109">Cmdleten **Get-AzKeyVaultCertificateContact** hämtar kontakter som är registrerade för certifikat aviseringar för ett huvud valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43869-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="43869-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43869-110">EXAMPLES</span></span>

### <span data-ttu-id="43869-111">Exempel 1: Hämta alla certifikat kontakter</span><span class="sxs-lookup"><span data-stu-id="43869-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="43869-112">Det här kommandot får alla kontakter för certifikat objekt i ett contoso-valv och lagrar dem sedan i $Contacts variabel.</span><span class="sxs-lookup"><span data-stu-id="43869-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="43869-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43869-113">PARAMETERS</span></span>

### <span data-ttu-id="43869-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43869-114">-DefaultProfile</span></span>
<span data-ttu-id="43869-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="43869-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43869-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43869-116">-InputObject</span></span>
<span data-ttu-id="43869-117">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="43869-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43869-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43869-118">-ResourceId</span></span>
<span data-ttu-id="43869-119">ID för valv.</span><span class="sxs-lookup"><span data-stu-id="43869-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="43869-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="43869-120">-VaultName</span></span>
<span data-ttu-id="43869-121">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="43869-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43869-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43869-122">CommonParameters</span></span>
<span data-ttu-id="43869-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43869-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43869-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43869-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43869-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43869-125">INPUTS</span></span>

### <span data-ttu-id="43869-126">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="43869-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="43869-127">System. String</span><span class="sxs-lookup"><span data-stu-id="43869-127">System.String</span></span>

## <span data-ttu-id="43869-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43869-128">OUTPUTS</span></span>

### <span data-ttu-id="43869-129">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="43869-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="43869-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43869-130">NOTES</span></span>

## <span data-ttu-id="43869-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43869-131">RELATED LINKS</span></span>

[<span data-ttu-id="43869-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="43869-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="43869-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="43869-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

