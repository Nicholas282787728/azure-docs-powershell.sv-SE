---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755415"
---
# <span data-ttu-id="22b56-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="22b56-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="22b56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22b56-102">SYNOPSIS</span></span>
<span data-ttu-id="22b56-103">Tar bort en Key Vault-tangenten från en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="22b56-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22b56-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22b56-105">DESCRIPTION</span></span>
<span data-ttu-id="22b56-106">Remove-AzureRmSqlServerKeyVaultKey cmdlet tar bort Key Vault-tangenten från den angivna SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="22b56-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="22b56-107">Observera att SQL Server-behörigheterna till Key-valvet inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="22b56-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="22b56-108">Använd set-AzureRmKeyVaultAccessPolicy för att ändra behörigheter.</span><span class="sxs-lookup"><span data-stu-id="22b56-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="22b56-109">Observera att denna cmdlet inte gör några ändringar i huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="22b56-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="22b56-110">Använd Remove-AzureKeyVaultKey om du vill ta bort en Key-valv.</span><span class="sxs-lookup"><span data-stu-id="22b56-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="22b56-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22b56-111">EXAMPLES</span></span>

### <span data-ttu-id="22b56-112">--------------------------Exempel 1: ta bort en Key valv-tangenten--------------------------</span><span class="sxs-lookup"><span data-stu-id="22b56-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="22b56-113">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="22b56-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="22b56-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="22b56-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="22b56-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22b56-115">PARAMETERS</span></span>

### <span data-ttu-id="22b56-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="22b56-116">-KeyId</span></span>
<span data-ttu-id="22b56-117">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="22b56-117">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b56-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b56-118">-ResourceGroupName</span></span>
<span data-ttu-id="22b56-119">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="22b56-119">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b56-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22b56-120">-ServerName</span></span>
<span data-ttu-id="22b56-121">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="22b56-121">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b56-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22b56-122">-Confirm</span></span>
<span data-ttu-id="22b56-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22b56-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b56-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b56-124">-WhatIf</span></span>
<span data-ttu-id="22b56-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22b56-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b56-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22b56-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b56-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b56-127">-DefaultProfile</span></span>
<span data-ttu-id="22b56-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22b56-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b56-129">CommonParameters</span></span>
<span data-ttu-id="22b56-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b56-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b56-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b56-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22b56-132">INPUTS</span></span>

### <span data-ttu-id="22b56-133">System. String</span><span class="sxs-lookup"><span data-stu-id="22b56-133">System.String</span></span>

## <span data-ttu-id="22b56-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22b56-134">OUTPUTS</span></span>

### <span data-ttu-id="22b56-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="22b56-135">System.Object</span></span>

## <span data-ttu-id="22b56-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22b56-136">NOTES</span></span>

## <span data-ttu-id="22b56-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22b56-137">RELATED LINKS</span></span>

[<span data-ttu-id="22b56-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="22b56-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
