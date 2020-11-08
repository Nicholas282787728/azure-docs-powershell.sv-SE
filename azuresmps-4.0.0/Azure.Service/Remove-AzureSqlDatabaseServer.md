---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099337"
---
# <span data-ttu-id="f232c-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f232c-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="f232c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f232c-102">SYNOPSIS</span></span>
<span data-ttu-id="f232c-103">Tar bort en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="f232c-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="f232c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f232c-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f232c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f232c-105">DESCRIPTION</span></span>
<span data-ttu-id="f232c-106">Cmdleten **Remove-AzureSqlDatabaseServer** tar bort den angivna instansen av Azure SQL Database Server från den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f232c-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="f232c-107">Denna cmdlet tar bort alla databaser på servern.</span><span class="sxs-lookup"><span data-stu-id="f232c-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="f232c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f232c-108">EXAMPLES</span></span>

### <span data-ttu-id="f232c-109">Exempel 1: ta bort en databas server</span><span class="sxs-lookup"><span data-stu-id="f232c-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="f232c-110">Det här kommandot tar bort Azure SQL-databasfilen med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="f232c-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="f232c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f232c-111">PARAMETERS</span></span>

### <span data-ttu-id="f232c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f232c-112">-Force</span></span>
<span data-ttu-id="f232c-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f232c-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f232c-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="f232c-114">-Profile</span></span>
<span data-ttu-id="f232c-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f232c-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f232c-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f232c-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f232c-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f232c-117">-ServerName</span></span>
<span data-ttu-id="f232c-118">Anger namnet på den server som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f232c-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="f232c-119">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="f232c-119">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f232c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f232c-120">-Confirm</span></span>
<span data-ttu-id="f232c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f232c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f232c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f232c-122">-WhatIf</span></span>
<span data-ttu-id="f232c-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f232c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f232c-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f232c-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f232c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f232c-125">CommonParameters</span></span>
<span data-ttu-id="f232c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f232c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f232c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f232c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f232c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f232c-128">INPUTS</span></span>

### <span data-ttu-id="f232c-129">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f232c-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="f232c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f232c-130">OUTPUTS</span></span>

## <span data-ttu-id="f232c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f232c-131">NOTES</span></span>

## <span data-ttu-id="f232c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f232c-132">RELATED LINKS</span></span>

[<span data-ttu-id="f232c-133">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="f232c-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f232c-134">Ta bort Server</span><span class="sxs-lookup"><span data-stu-id="f232c-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="f232c-135">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f232c-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f232c-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f232c-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f232c-137">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f232c-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f232c-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f232c-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


