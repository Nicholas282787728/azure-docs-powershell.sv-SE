---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415931"
---
# <span data-ttu-id="d08de-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d08de-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="d08de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d08de-102">SYNOPSIS</span></span>
<span data-ttu-id="d08de-103">Hämtar en SQL-Servers nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="d08de-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="d08de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d08de-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d08de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d08de-105">DESCRIPTION</span></span>
<span data-ttu-id="d08de-106">Get-AzSqlServerKeyVaultKey-cmdleten hämtar information om nyckel valv nycklar på en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="d08de-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="d08de-107">Du kan visa alla nycklar på en server eller Visa en specifik nyckel genom att ange KeyId.</span><span class="sxs-lookup"><span data-stu-id="d08de-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="d08de-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d08de-108">EXAMPLES</span></span>

### <span data-ttu-id="d08de-109">Exempel 1: Hämta alla nyckel valv nycklar</span><span class="sxs-lookup"><span data-stu-id="d08de-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d08de-110">Det här kommandot får alla nyckel valv nycklar på en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="d08de-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="d08de-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am ResourceGroupName: ContosoResourceGroup servername: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 tumavtryck: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="d08de-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="d08de-112">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="d08de-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d08de-113">Det här kommandot får Key Vault-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' och lagrar det sedan i $MyServerKeyVaultKey variabel.</span><span class="sxs-lookup"><span data-stu-id="d08de-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="d08de-114">Du kan kontrol lera egenskaperna för $MyServerKeyVaultKey för att få information om nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="d08de-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="d08de-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d08de-115">PARAMETERS</span></span>

### <span data-ttu-id="d08de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08de-116">-DefaultProfile</span></span>
<span data-ttu-id="d08de-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d08de-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d08de-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d08de-118">-KeyId</span></span>
<span data-ttu-id="d08de-119">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d08de-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08de-120">-ResourceGroupName</span></span>
<span data-ttu-id="d08de-121">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d08de-121">The name of the resource group</span></span>

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

### <span data-ttu-id="d08de-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d08de-122">-ServerName</span></span>
<span data-ttu-id="d08de-123">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="d08de-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d08de-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d08de-124">-Confirm</span></span>
<span data-ttu-id="d08de-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d08de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d08de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d08de-126">-WhatIf</span></span>
<span data-ttu-id="d08de-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d08de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d08de-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d08de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d08de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08de-129">CommonParameters</span></span>
<span data-ttu-id="d08de-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08de-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d08de-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08de-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d08de-132">INPUTS</span></span>

### <span data-ttu-id="d08de-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d08de-133">System.String</span></span>

## <span data-ttu-id="d08de-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d08de-134">OUTPUTS</span></span>

### <span data-ttu-id="d08de-135">Microsoft. Azure. commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="d08de-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="d08de-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d08de-136">NOTES</span></span>

## <span data-ttu-id="d08de-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d08de-137">RELATED LINKS</span></span>

[<span data-ttu-id="d08de-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d08de-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
