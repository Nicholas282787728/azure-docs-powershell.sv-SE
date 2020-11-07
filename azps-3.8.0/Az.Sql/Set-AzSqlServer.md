---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925902"
---
# <span data-ttu-id="9de84-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="9de84-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="9de84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9de84-102">SYNOPSIS</span></span>
<span data-ttu-id="9de84-103">Ändrar egenskaper för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="9de84-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="9de84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9de84-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9de84-105">DESCRIPTION</span></span>
<span data-ttu-id="9de84-106">Cmdleten **set-AzSqlServer** ändrar egenskaper för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="9de84-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="9de84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9de84-107">EXAMPLES</span></span>

### <span data-ttu-id="9de84-108">Exempel 1: återställa administratörs lösen ordet</span><span class="sxs-lookup"><span data-stu-id="9de84-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="9de84-109">Det här kommandot återställer administratörs lösen ordet på AzureSQL-servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="9de84-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="9de84-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9de84-110">PARAMETERS</span></span>

### <span data-ttu-id="9de84-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9de84-111">-AssignIdentity</span></span>
<span data-ttu-id="9de84-112">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="9de84-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9de84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de84-113">-DefaultProfile</span></span>
<span data-ttu-id="9de84-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9de84-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9de84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9de84-115">-Force</span></span>
<span data-ttu-id="9de84-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9de84-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9de84-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9de84-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="9de84-118">Tar en flagga som är aktive rad eller inaktiv för att ange om offentliga nätverks åtkomst till servern tillåts eller inte.</span><span class="sxs-lookup"><span data-stu-id="9de84-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="9de84-119">När det är inaktiverat kan bara anslutningar som görs med privata länkar nå den här servern.</span><span class="sxs-lookup"><span data-stu-id="9de84-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de84-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de84-120">-ResourceGroupName</span></span>
<span data-ttu-id="9de84-121">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="9de84-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9de84-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9de84-122">-ServerName</span></span>
<span data-ttu-id="9de84-123">Anger namnet på den server som cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="9de84-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de84-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9de84-124">-ServerVersion</span></span>
<span data-ttu-id="9de84-125">Anger den version som den här cmdleten ändrar till servern.</span><span class="sxs-lookup"><span data-stu-id="9de84-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="9de84-126">De acceptabla värdena för den här parametern är: 2,0 och 12,0.</span><span class="sxs-lookup"><span data-stu-id="9de84-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de84-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="9de84-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="9de84-128">Anger ett nytt lösen ord som en **SecureString** för databas Server administratören.</span><span class="sxs-lookup"><span data-stu-id="9de84-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="9de84-129">Använd Get-Credential cmdlet för att få en **SecureString**.</span><span class="sxs-lookup"><span data-stu-id="9de84-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="9de84-130">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9de84-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de84-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9de84-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="9de84-132">Den minsta TLS-version som ska tillämpas för SQL Server</span><span class="sxs-lookup"><span data-stu-id="9de84-132">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de84-133">-Taggar</span><span class="sxs-lookup"><span data-stu-id="9de84-133">-Tags</span></span>
<span data-ttu-id="9de84-134">Anger en ord lista med taggar som denna cmdlet associerar med servern.</span><span class="sxs-lookup"><span data-stu-id="9de84-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="9de84-135">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="9de84-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9de84-136">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="9de84-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de84-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9de84-137">-Confirm</span></span>
<span data-ttu-id="9de84-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9de84-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de84-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de84-139">-WhatIf</span></span>
<span data-ttu-id="9de84-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9de84-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de84-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9de84-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de84-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de84-142">CommonParameters</span></span>
<span data-ttu-id="9de84-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de84-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de84-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9de84-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de84-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9de84-145">INPUTS</span></span>

### <span data-ttu-id="9de84-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9de84-146">System.String</span></span>

## <span data-ttu-id="9de84-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9de84-147">OUTPUTS</span></span>

### <span data-ttu-id="9de84-148">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9de84-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="9de84-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9de84-149">NOTES</span></span>

## <span data-ttu-id="9de84-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9de84-150">RELATED LINKS</span></span>

[<span data-ttu-id="9de84-151">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9de84-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
