---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 81ec18dd543a63a971d01a64c878774b266cf0fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584851"
---
# <span data-ttu-id="5a04c-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a04c-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5a04c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a04c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a04c-103">Tar bort en Key Vault-tangenten från en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="5a04c-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a04c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a04c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a04c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a04c-105">DESCRIPTION</span></span>
<span data-ttu-id="5a04c-106">Remove-AzureRmSqlServerKeyVaultKey cmdlet tar bort Key Vault-tangenten från den angivna SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="5a04c-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="5a04c-107">Observera att SQL Server-behörigheterna till Key-valvet inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="5a04c-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="5a04c-108">Använd set-AzureRmKeyVaultAccessPolicy för att ändra behörigheter.</span><span class="sxs-lookup"><span data-stu-id="5a04c-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="5a04c-109">Observera att denna cmdlet inte gör några ändringar i huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="5a04c-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="5a04c-110">Använd Remove-AzureKeyVaultKey om du vill ta bort en Key-valv.</span><span class="sxs-lookup"><span data-stu-id="5a04c-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="5a04c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a04c-111">EXAMPLES</span></span>

### <span data-ttu-id="5a04c-112">Exempel 1: ta bort en Key valv-tangenten</span><span class="sxs-lookup"><span data-stu-id="5a04c-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5a04c-113">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="5a04c-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="5a04c-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="5a04c-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="5a04c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a04c-115">PARAMETERS</span></span>

### <span data-ttu-id="5a04c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a04c-116">-AsJob</span></span>
<span data-ttu-id="5a04c-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5a04c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a04c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a04c-118">-DefaultProfile</span></span>
<span data-ttu-id="5a04c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5a04c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a04c-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5a04c-120">-KeyId</span></span>
<span data-ttu-id="5a04c-121">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5a04c-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="5a04c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a04c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a04c-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5a04c-123">The name of the resource group</span></span>

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

### <span data-ttu-id="5a04c-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a04c-124">-ServerName</span></span>
<span data-ttu-id="5a04c-125">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="5a04c-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5a04c-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a04c-126">-Confirm</span></span>
<span data-ttu-id="5a04c-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a04c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a04c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a04c-128">-WhatIf</span></span>
<span data-ttu-id="5a04c-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a04c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a04c-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a04c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a04c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a04c-131">CommonParameters</span></span>
<span data-ttu-id="5a04c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a04c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a04c-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a04c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a04c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a04c-134">INPUTS</span></span>

### <span data-ttu-id="5a04c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5a04c-135">System.String</span></span>

## <span data-ttu-id="5a04c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a04c-136">OUTPUTS</span></span>

### <span data-ttu-id="5a04c-137">Microsoft. Azure. commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5a04c-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5a04c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a04c-138">NOTES</span></span>

## <span data-ttu-id="5a04c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a04c-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a04c-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5a04c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
