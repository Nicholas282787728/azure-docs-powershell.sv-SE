---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088993"
---
# <span data-ttu-id="4be50-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4be50-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="4be50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4be50-102">SYNOPSIS</span></span>
<span data-ttu-id="4be50-103">Lägger till en Key valv-nycklar i en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="4be50-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="4be50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4be50-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be50-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4be50-105">DESCRIPTION</span></span>
<span data-ttu-id="4be50-106">Add-AzSqlServerKeyVaultKey-cmdleten lägger till en Key valv-nycklar till den medföljande SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="4be50-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="4be50-107">Servern måste ha behörigheten get, wrapKey, unwrapKey för valvet.</span><span class="sxs-lookup"><span data-stu-id="4be50-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="4be50-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4be50-108">EXAMPLES</span></span>

### <span data-ttu-id="4be50-109">Exempel 1: Lägg till Key valv-tangenten</span><span class="sxs-lookup"><span data-stu-id="4be50-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="4be50-110">Det här kommandot lägger till Key Vault-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' på SQL Server med namnet "ContosoServer" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4be50-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="4be50-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="4be50-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="4be50-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4be50-112">PARAMETERS</span></span>

### <span data-ttu-id="4be50-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4be50-113">-AsJob</span></span>
<span data-ttu-id="4be50-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4be50-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4be50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be50-115">-DefaultProfile</span></span>
<span data-ttu-id="4be50-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4be50-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4be50-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4be50-117">-KeyId</span></span>
<span data-ttu-id="4be50-118">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4be50-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="4be50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be50-119">-ResourceGroupName</span></span>
<span data-ttu-id="4be50-120">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4be50-120">The name of the resource group</span></span>

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

### <span data-ttu-id="4be50-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4be50-121">-ServerName</span></span>
<span data-ttu-id="4be50-122">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="4be50-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4be50-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4be50-123">-Confirm</span></span>
<span data-ttu-id="4be50-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4be50-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be50-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be50-125">-WhatIf</span></span>
<span data-ttu-id="4be50-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4be50-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be50-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4be50-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be50-128">CommonParameters</span></span>
<span data-ttu-id="4be50-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be50-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4be50-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be50-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4be50-131">INPUTS</span></span>

### <span data-ttu-id="4be50-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4be50-132">System.String</span></span>

## <span data-ttu-id="4be50-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4be50-133">OUTPUTS</span></span>

### <span data-ttu-id="4be50-134">Microsoft. Azure. commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="4be50-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="4be50-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4be50-135">NOTES</span></span>

## <span data-ttu-id="4be50-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4be50-136">RELATED LINKS</span></span>

[<span data-ttu-id="4be50-137">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4be50-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
